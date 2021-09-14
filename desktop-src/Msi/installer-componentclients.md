---
description: La propiedad ComponentClients de solo lectura devuelve un objeto StringList que enumera el conjunto de clientes de un componente especificado.
ms.assetid: 47553360-298f-4be8-819d-18f4df96667c
title: Installer.ComponentClients, propiedad
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171730"
---
# <a name="installercomponentclients-property"></a>Installer.ComponentClients, propiedad

La propiedad **ComponentClients de solo** lectura devuelve un [**objeto StringList**](stringlist-object.md) que enumera el conjunto de clientes de un componente especificado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.ComponentClients
```



## <a name="property-value"></a>Valor de propiedad

GUID de cadena que representa el código de componente del componente. Los códigos de componente se especifican en la columna ComponentId de la [tabla Component](component-table.md).

## <a name="remarks"></a>Observaciones

Para enumerar los clientes de componentes, una aplicación puede recorrer en iteración el [**objeto StringList**](stringlist-object.md) mediante una construcción For Each. Dado que los clientes no están ordenados, los nuevos componentes tienen un índice arbitrario. Esto significa que la función puede devolver clientes en cualquier orden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)
</dt> </dl>

 

 




