---
description: La propiedad ComponentRequestState del objeto de sesión obtiene o solicita un cambio en el estado de acción de una fila de la tabla de componentes.
ms.assetid: d0b50c25-dca6-4bdf-8ee9-490e436fcc5b
title: Propiedad Session. ComponentRequestState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 17ec77c5498a808e0d7ac0f2881057979d7db0c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680411"
---
# <a name="sessioncomponentrequeststate-property"></a>Propiedad Session. ComponentRequestState

La propiedad **ComponentRequestState** del objeto de [**sesión**](session-object.md) obtiene o solicita un cambio en el estado de acción de una fila de la [tabla de componentes](component-table.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.ComponentRequestState
```



## <a name="property-value"></a>Valor de propiedad

Nombre de cadena necesario del elemento de componente, clave principal de la tabla de componentes.

## <a name="remarks"></a>Observaciones



| Estado de selección        | Value | Descripción                                                    |
|------------------------|-------|----------------------------------------------------------------|
| Null                   | Null  | Solicita que no se realice ninguna acción para este elemento.                |
| msiInstallStateAbsent  | 2     | Se va a quitar el elemento.                                         |
| msiInstallStateLocal   | 3     | El elemento se instalará localmente.                               |
| msiInstallStateSource  | 4     | El elemento debe instalarse y ejecutarse desde el medio de origen.         |
| msiInstallStateDefault | 5     | Si está instalado, el elemento se debe volver a instalar en el mismo estado. |



 

Si se produce un error en la propiedad, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




