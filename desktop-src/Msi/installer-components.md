---
description: La propiedad componentes de solo lectura devuelve un objeto StringList que enumera el conjunto de componentes instalados para todos los productos.
ms.assetid: c84e4329-428a-440a-bd65-097588a86932
title: Installer. Components (propiedad)
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
ms.openlocfilehash: e6767be5182b15836c071bf8b00ed8441f6031dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653802"
---
# <a name="installercomponents-property"></a>Installer. Components (propiedad)

La propiedad **componentes** de solo lectura devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de componentes instalados para todos los productos.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.Components
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Para enumerar los componentes, una aplicación puede recorrer en iteración el objeto [**StringList**](stringlist-object.md) mediante una construcción for each. Dado que los componentes no están ordenados, los componentes nuevos tienen un índice arbitrario. Esto significa que la función puede devolver componentes en cualquier orden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)
</dt> </dl>

 

 




