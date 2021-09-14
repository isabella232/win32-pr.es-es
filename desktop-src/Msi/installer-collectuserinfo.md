---
description: El método CollectUserInfo del objeto Installer invoca una secuencia del asistente de interfaz de usuario que recopila y almacena la información del usuario y el código de producto.
ms.assetid: 2faacf38-1af1-4e8a-a3f6-87733104614e
title: Método Installer.CollectUserInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CollectUserInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d7286fdbc9fab6b3db6752284bf86db05f920bd7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171737"
---
# <a name="installercollectuserinfo-method"></a>Método Installer.CollectUserInfo

El **método CollectUserInfo** del objeto [**Installer**](installer-object.md) invoca una secuencia del asistente de interfaz de usuario que recopila y almacena la información del usuario y el código de producto.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.CollectUserInfo(
  Product
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Producto* 
</dt> <dd>

Especifica el código [**de producto**](productcode.md) del producto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una aplicación debe llamar al **método CollectUserInfo** la primera vez que se ejecuta. El **método CollectUserInfo** abre el paquete de instalación del producto e invoca una secuencia del asistente de interfaz de usuario que recopila información del usuario. Tras la finalización de la secuencia del asistente, se registra la información de usuario recopilada. La [**propiedad UILevel**](installer-uilevel.md) debe establecerse en msiUILevelFull porque esta API requiere una interfaz de usuario de creación.

El **método CollectUserInfo** invoca el [cuadro de diálogo FirstRun](firstrun-dialog.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
</dt> </dl>

 

 




