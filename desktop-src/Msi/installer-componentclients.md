---
description: La propiedad ComponentClients de solo lectura devuelve un objeto StringList que enumera el conjunto de clientes de un componente especificado.
ms.assetid: 47553360-298f-4be8-819d-18f4df96667c
title: Propiedad Installer. ComponentClients
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentClients
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2241babae283f367a15c8f742b51af280ed1a3b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653695"
---
# <a name="installercomponentclients-property"></a>Propiedad Installer. ComponentClients

La propiedad **ComponentClients** de solo lectura devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de clientes de un componente especificado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.ComponentClients
```



## <a name="property-value"></a>Valor de propiedad

GUID de cadena que representa el código de componente del componente. Los códigos de componente se especifican en la columna ComponentId de la [tabla de componentes](component-table.md).

## <a name="remarks"></a>Observaciones

Para enumerar los clientes de componentes, una aplicación puede recorrer en iteración el objeto [**StringList**](stringlist-object.md) mediante una construcción for each. Dado que los clientes no están ordenados, todos los componentes nuevos tienen un índice arbitrario. Esto significa que la función puede devolver los clientes en cualquier orden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)
</dt> </dl>

 

 




