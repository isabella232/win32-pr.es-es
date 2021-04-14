---
description: El método OpenProduct del objeto Installer abre un paquete de instalador para un producto instalado mediante el código de producto y devuelve un objeto de sesión.
ms.assetid: f09c4795-19e1-4474-b7ca-68ef650b69d5
title: Instalador. OpenProduct (método)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653899"
---
# <a name="installeropenproduct-method"></a>Instalador. OpenProduct (método)

El método **OpenProduct** del objeto [**Installer**](installer-object.md) abre un paquete de instalador para un producto instalado mediante el código de producto y devuelve un objeto de [**sesión**](session-object.md) .

## <a name="syntax"></a>Sintaxis


```JScript
Installer.OpenProduct(
  productCode
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*productCode* 
</dt> <dd>

Cadena requerida que contiene el código de producto único (un [GUID](guid.md)) o un descriptor de activación escrito por el instalador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Tenga en cuenta que solo un único proceso puede abrir un objeto de [**sesión**](session-object.md) . **OpenProduct** no se puede usar en una acción personalizada porque la instalación activa es la única sesión permitida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




