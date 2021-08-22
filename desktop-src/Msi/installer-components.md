---
description: La propiedad Components de solo lectura devuelve un objeto StringList que enumera el conjunto de componentes instalados para todos los productos.
ms.assetid: c84e4329-428a-440a-bd65-097588a86932
title: Installer.Components, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Components
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b8538e594ed02a1bc355ed4cf57db1befb1443e58d7afe2038b16e08eb9e4659
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632413"
---
# <a name="installercomponents-property"></a>Installer.Components, propiedad

La propiedad **Components** de solo lectura devuelve [**un objeto StringList**](stringlist-object.md) que enumera el conjunto de componentes instalados para todos los productos.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.Components
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

Para enumerar los componentes, una aplicación puede recorrer en iteración el [**objeto StringList**](stringlist-object.md) mediante una construcción For Each. Dado que los componentes no están ordenados, los componentes nuevos tienen un índice arbitrario. Esto significa que la función puede devolver componentes en cualquier orden.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)
</dt> </dl>

 

 




