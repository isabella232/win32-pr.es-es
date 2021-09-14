---
description: El método OpenProduct del objeto Installer abre un paquete de instalador para un producto instalado mediante el código de producto y devuelve un objeto Session.
ms.assetid: f09c4795-19e1-4474-b7ca-68ef650b69d5
title: Método Installer.OpenProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9fd25a1f204a6d42cd4cb6e330d7d69da2cddb07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072132"
---
# <a name="installeropenproduct-method"></a>Método Installer.OpenProduct

El **método OpenProduct** del objeto [**Installer**](installer-object.md) abre un paquete de instalador para un producto instalado mediante el código de producto y devuelve un [**objeto Session.**](session-object.md)

## <a name="syntax"></a>Sintaxis


```JScript
Installer.OpenProduct(
  productCode
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Productcode* 
</dt> <dd>

Cadena obligatoria que contiene el código de producto único [(un GUID)](guid.md)o un descriptor de activación escrito por el instalador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Tenga en cuenta que solo [**un proceso**](session-object.md) puede abrir un objeto Session. **OpenProduct** no se puede usar en una acción personalizada porque la instalación activa es la única sesión permitida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




