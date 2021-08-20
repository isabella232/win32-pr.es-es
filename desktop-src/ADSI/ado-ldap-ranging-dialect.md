---
title: Dialecto de rango LDAP de ADO
description: Al usar ActiveX Directory Objects (ADO) con el dialecto LDAP, el atributo y el especificador de intervalo no requieren comillas.
ms.assetid: adda9cf7-6588-48ee-85e2-fddbaf28807b
ms.tgt_platform: multiple
keywords:
- ADSI de dialecto de rango LDAP de ADO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15dba9b7a701b792321ef327d7b5f9893ef3daa0a5eaad80ea151c2b2c90cad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023993"
---
# <a name="ado-ldap-ranging-dialect"></a>Dialecto de rango LDAP de ADO

Al usar ActiveX Directory Objects (ADO) con el dialecto LDAP, el atributo y el especificador de intervalo no requieren comillas.

A continuación se muestra un ejemplo del dialecto LDAP de ADO.


```C++
Command.Text = "<LDAP://CN=NewGroup,DC=Fabrikam,DC=Com>;(objectCategory=group);name,member;Range=51-*;base"
```



 

 




