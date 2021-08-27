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
ms.openlocfilehash: 3aa6176b297261968a63b2f723a65ea14b45b8d3628b200be92df556adc5c2b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129385"
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

## <a name="remarks"></a>Comentarios

Tenga en cuenta que solo [**un proceso**](session-object.md) puede abrir un objeto Session. **OpenProduct** no se puede usar en una acción personalizada porque la instalación activa es la única sesión permitida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




