---
description: El método AddSource del objeto de instalador agrega un origen a la lista de orígenes de red válidos en el SourceList.
ms.assetid: e24c8484-fe84-4f97-9c06-c063bb7c6810
title: Instalador. AddSource (método)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653624"
---
# <a name="installeraddsource-method"></a>Instalador. AddSource (método)

El método **AddSource** del objeto de [**instalador**](installer-object.md) agrega un origen a la lista de orígenes de red válidos en el SourceList.

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

Nombre de usuario para la instalación por usuario; cadena nula o vacía para la instalación por máquina.

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
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)
</dt> <dt>

[resistencia de origen](source-resiliency.md)
</dt> </dl>

 

 




