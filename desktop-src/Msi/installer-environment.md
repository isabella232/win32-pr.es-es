---
description: La propiedad Environment del objeto Installer es una propiedad de lectura y escritura que es el valor de cadena de una variable de entorno del proceso actual.
ms.assetid: f59a270f-9bd8-4d17-96e2-cb3c62a31cad
title: Installer.Environment, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Environment
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3983eceecd8bc709bea4a094c61c9886c73def3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171670"
---
# <a name="installerenvironment-property"></a>Installer.Environment, propiedad

La **propiedad Environment** del objeto [**Installer**](installer-object.md) es una propiedad de lectura y escritura que es el valor de cadena de una variable de entorno del proceso actual.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.Environment
Installer.Environment = propVal 
```



## <a name="property-value"></a>Valor de propiedad

Nombre de la variable de entorno que se va a leer o escribir. Esto no tiene en cuenta las mayúsculas y minúsculas.

## <a name="remarks"></a>Observaciones

Establecer una variable de entorno con **la propiedad Entorno** solo afecta a la sesión activa. Para realizar cambios persistentes en una variable de entorno, use la [tabla Environment](environment-table.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




