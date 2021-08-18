---
description: La propiedad ComponentRequestState del objeto Session obtiene o solicita un cambio en el estado Action de una fila de la tabla Component.
ms.assetid: d0b50c25-dca6-4bdf-8ee9-490e436fcc5b
title: Propiedad Session.ComponentRequestState
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
ms.openlocfilehash: 3cef17ab3a4781f925e92968bd50dfedddd9a0df8e1781a2f209712fc447ef10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625241"
---
# <a name="sessioncomponentrequeststate-property"></a>Propiedad Session.ComponentRequestState

La **propiedad ComponentRequestState** del objeto [**Session**](session-object.md) obtiene o solicita un cambio en el estado Action de una fila de la [tabla Component](component-table.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.ComponentRequestState
```



## <a name="property-value"></a>Valor de propiedad

Nombre de cadena requerido del elemento de componente, clave principal de la tabla Component.

## <a name="remarks"></a>Comentarios



| Estado de selección        | Valor | Descripción                                                    |
|------------------------|-------|----------------------------------------------------------------|
| Null                   | Null  | Solicita que no se haya realizado ninguna acción para este elemento.                |
| msiInstallStateAbsent  | 2     | El elemento se va a quitar.                                         |
| msiInstallStateLocal   | 3     | El elemento se va a instalar localmente.                               |
| msiInstallStateSource  | 4     | El elemento se va a instalar y ejecutar desde el medio de origen.         |
| msiInstallStateDefault | 5     | Si está instalado, el elemento se reinstalará en el mismo estado. |



 

Si se produce un error en la propiedad , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession se define como \_ 000C109E-0000-0000-C000-00000000046<br/>                                                                                                                                                                             |



 

 




