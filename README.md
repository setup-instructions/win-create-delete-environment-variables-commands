# Criar variável de sistema
```
setx VAR1 "valor1" /M
```

# Criar variável de usuário
```
setx VAR1 "valor1"
```

# Excluir variável de sistema
```
setx VAR1 "" /M
REG DELETE "HKLM\SYSTEM\CurrentControlSet\Control\Session Manager\Environment" /v VAR1 /f
```

# Excluir variável de usuário
setx VAR1 ""
REG DELETE "HKEY_CURRENT_USER\Environment" /v VAR1 /f

# C# - Ler variável de sustema
```
string path = Environment.GetEnvironmentVariable("PATH");
```

# C# - Ler variável de usuário
```
string var1 = Environment.GetEnvironmentVariable("VAR1", EnvironmentVariableTarget.User);
```