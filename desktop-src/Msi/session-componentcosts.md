---
description: La propiedad ComponentCosts del objeto de sesión devuelve un objeto RecordList que enumera el espacio en disco por unidad necesaria para instalar un componente.
ms.assetid: 9b1355f1-cc99-49d9-8187-07fba4804d1f
title: Propiedad Session. ComponentCosts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCosts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a6ef4e3bfd441f5de61c0f3d69aea93d6cfd2ed8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679523"
---
# <a name="sessioncomponentcosts-property"></a>Propiedad Session. ComponentCosts

La propiedad ComponentCosts del objeto de [**sesión**](session-object.md) devuelve un objeto [**RecordList**](recordlist-object.md) que enumera el espacio en disco por unidad necesaria para instalar un componente. La interfaz de usuario usa esta información para mostrar el espacio en disco necesario para todas las unidades. Los costos de espacio en disco devueltos son múltiplos de 512 bytes.

La propiedad ComponentCosts solo debe usarse después de que el instalador haya completado el [costo de archivos](file-costing.md) y después de la [acción CostFinalize](costfinalize-action.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.ComponentCosts
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Para obtener el costo total, agregue los costos de todos los componentes más el costo del motor de instalación (componente = "").

ComponentCosts devuelve un [**objeto RecordList**](recordlist-object.md). Cada registro del objeto RecordList devuelto tiene los siguientes campos:



| Campo | Descripción                                          |
|-------|------------------------------------------------------|
| 1     | Nombre de volumen o unidad                                    |
| 2     | Costo final de espacio en disco en múltiplos de 512 bytes.     |
| 3     | Costo de espacio en disco temporal en múltiplos de 512 bytes. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




