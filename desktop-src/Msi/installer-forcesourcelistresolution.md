---
description: El método ForceSourceListResolution del objeto de instalador obliga al Windows Installer a buscar en la lista de origen un origen de producto válido.
ms.assetid: d5097331-8cf5-494f-9e88-bcffcad3fe5d
title: Instalador. ForceSourceListResolution (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ForceSourceListResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cadc27f3eaa90cd6fb2729f73d07cbcfa1f96b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653329"
---
# <a name="installerforcesourcelistresolution-method"></a>Instalador. ForceSourceListResolution (método)

El método **ForceSourceListResolution** del objeto de [**instalador**](installer-object.md) obliga al instalador a buscar en la lista de origen un origen de producto válido la próxima vez que se necesite un origen, por ejemplo, cuando el instalador realiza una instalación o una reinstalación, o cuando necesita la ruta de acceso de un conjunto de componentes para que se ejecute desde el origen.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.ForceSourceListResolution(
  Product,
  User
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

[**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[Resistencia de origen](source-resiliency.md)
</dt> </dl>

 

 




