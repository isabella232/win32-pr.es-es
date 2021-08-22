---
description: El método ForceSourceListResolution del objeto Installer fuerza al instalador de Windows a buscar en la lista de origen un origen de producto válido.
ms.assetid: d5097331-8cf5-494f-9e88-bcffcad3fe5d
title: Método Installer.ForceSourceListResolution
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
ms.openlocfilehash: cafff03a392fc1977fd19b5b8415ca499d614c2c4ba3fb4f7104edd5344f3a86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630597"
---
# <a name="installerforcesourcelistresolution-method"></a>Método Installer.ForceSourceListResolution

El **método ForceSourceListResolution** del objeto [**Installer**](installer-object.md) obliga al instalador a buscar en la lista de origen un origen de producto válido la próxima vez que se necesite un origen, como cuando el instalador realiza una instalación o una reinstalación, o cuando necesita la ruta de acceso para que un componente establecido se ejecute desde el origen.

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

Nombre de usuario para la instalación por usuario; Cadena nula o vacía para la instalación por máquina.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[Resistencia de origen](source-resiliency.md)
</dt> </dl>

 

 




