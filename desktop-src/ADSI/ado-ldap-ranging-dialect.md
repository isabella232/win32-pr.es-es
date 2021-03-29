---
title: Lenguaje de dialecto de ADO LDAP
description: Al utilizar objetos de directorio ActiveX (ADO) con el dialecto LDAP, el especificador de atributo y de intervalo no requiere comillas.
ms.assetid: adda9cf7-6588-48ee-85e2-fddbaf28807b
ms.tgt_platform: multiple
keywords:
- Lenguaje LDAP de ADO que abarca ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78dc2c7ff2dbfc81a76ff582145b7cf12916439
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903086"
---
# <a name="ado-ldap-ranging-dialect"></a><span data-ttu-id="90ffd-104">Lenguaje de dialecto de ADO LDAP</span><span class="sxs-lookup"><span data-stu-id="90ffd-104">ADO LDAP Ranging Dialect</span></span>

<span data-ttu-id="90ffd-105">Al utilizar objetos de directorio ActiveX (ADO) con el dialecto LDAP, el especificador de atributo y de intervalo no requiere comillas.</span><span class="sxs-lookup"><span data-stu-id="90ffd-105">When using ActiveX Directory Objects (ADO) with the LDAP dialect, the attribute and range specifier do not require quotation marks.</span></span>

<span data-ttu-id="90ffd-106">El siguiente es un ejemplo del dialecto LDAP de ADO.</span><span class="sxs-lookup"><span data-stu-id="90ffd-106">The following is an example of the ADO LDAP dialect.</span></span>


```C++
Command.Text = "<LDAP://CN=NewGroup,DC=Fabrikam,DC=Com>;(objectCategory=group);name,member;Range=51-*;base"
```



 

 




