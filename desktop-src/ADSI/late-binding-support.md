---
title: Compatibilidad con enlaces en tiempo de tarde
description: Cuando la compatibilidad con el enlace en tiempo de tarde está en su lugar, cada llamada de función debe pasar a través de la interfaz ADSI IDispatch, antes de que se vuelva a enrutar a la extensión adecuada.
ms.assetid: fbdc6234-9381-4d64-bf02-05e393b3e0bd
ms.tgt_platform: multiple
keywords:
- extensiones ADSI, compatibilidad con enlaces en tiempo de tarde
- ADSI ADSI, código de ejemplo Visual Basic compatibilidad con enlaces en tiempo de tarde
- enlace de AD, compatibilidad con enlaces en tiempo de tarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff8a66764e49e912e7d4db61356c997516b8d2192046912e673640e9567e415
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821325"
---
# <a name="late-binding-support"></a>Compatibilidad con enlaces en tiempo de tarde

Cuando la compatibilidad con el enlace en tiempo de tarde está en su lugar, cada llamada de función debe pasar a través de la interfaz [**ADSI IDispatch,**](/windows/win32/api/oaidl/nn-oaidl-idispatch) antes de que se vuelva a enrutar a la extensión adecuada.

Tenga en cuenta el siguiente código de ejemplo.


```C++
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
 
x.MyNewMethod( "\\srv\public")
x.MyProperty = "Hello World"
 
x.OtherMethod()
x.OtherProperty = 4362
 
Debug.Print x.LastName
```



No hay llamadas explícitas al **método QueryInterface** para llegar a las extensiones. Las extensiones deben redirigir sus llamadas [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) a la interfaz **ADSI IDispatch.** ADSI toma la decisión y resuelve los conflictos que se producen y, a continuación, vuelve a enrutar a la extensión adecuada mediante una interfaz denominada [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension). Por lo tanto, cualquier extensión que admita el enlace en tiempo de ejecución debe implementar **IADsExtension**.

 

 