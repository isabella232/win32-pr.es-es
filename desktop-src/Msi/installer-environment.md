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
ms.openlocfilehash: 8f24237da6c140ef0d38ff17591bf214698cfa6731bd4e8d3cfcaa613b335404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631691"
---
# <a name="installerenvironment-property"></a>Installer.Environment, propiedad

La **propiedad Environment** del objeto [**Installer**](installer-object.md) es una propiedad de lectura y escritura que es el valor de cadena de una variable de entorno del proceso actual.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.Environment
Installer.Environment = propVal 
```



## <a name="property-value"></a>Valor de propiedad

Nombre de la variable de entorno que se va a leer o escribir. Esto no tiene en cuenta las mayúsculas y minúsculas.

## <a name="remarks"></a>Comentarios

Establecer una variable de entorno con **la propiedad Entorno** solo afecta a la sesión activa. Para realizar cambios persistentes en una variable de entorno, use la [tabla Environment](environment-table.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




