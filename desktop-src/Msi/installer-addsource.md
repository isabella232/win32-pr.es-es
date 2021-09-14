---
description: El método AddSource del objeto Installer agrega un origen a la lista de orígenes de red válidos en sourcelist.
ms.assetid: e24c8484-fe84-4f97-9c06-c063bb7c6810
title: Installer.AddSource (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3067ae287311c6ed26b509545523db75a3fed4cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171761"
---
# <a name="installeraddsource-method"></a>Installer.AddSource (método)

El **método AddSource** del objeto [**Installer**](installer-object.md) agrega un origen a la lista de orígenes de red válidos en sourcelist.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.AddSource(
  Product,
  User,
  Source
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Producto* 
</dt> <dd>

Especifica el código de producto.

</dd> <dt>

*User* 
</dt> <dd>

Nombre de usuario para la instalación por usuario; Cadena nula o vacía para la instalación por equipo.

</dd> <dt>

*Origen* 
</dt> <dd>

Puntero a la cadena que especifica el origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)
</dt> <dt>

[resistencia de origen](source-resiliency.md)
</dt> </dl>

 

 




