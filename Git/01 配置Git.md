# 配置Git

### **配置文件**

通过 `git config` 命令配置 git 的一些变量。 这些变量一般存在三个不同的位置：
1. `[path]/etc/gitconfig` ：包含着对于计算机上每个用户和每个 repo 都生效的全局配置。对本机上所有repo的默认配置生效。通过 `git config --system` 来进行配置。由于这个文件是一个系统设置文件，你需要提权之后方能配置。
2. `~/.gitconfig` 或者 `~/.config/git/config` ：在当前 user 下使用的配置文件。对此 user 下的所有 repo 的默认配置生效。你可以通过 `git config --global` 来对这个文件进行配置。
3. `.git/config` ：在当前 repo 下使用的配置文件。通过 `git config --local`配置。需要在 repo 文件夹内进行配置才能生效。

+ **覆盖关系：local -> global -> system 从左向右覆盖。**

### **身份信息**

* 配置用户名： `git config --global 'UserName'`
  
* 配置用户邮箱： `git config --global 'UserMail@example.com'`
  
这些信息一经配置，无须再次修改。

### **默认主干**
        
git 的默认主干是 `master` 。你可以通过指令 `git config --global init.defaultBranch BranchName` 来自定义默认主干的名称。

### **检查设置**

* 通过 `git config --list` 来检查所有配置
* 通过 `git config <key>`  以检查特定配置