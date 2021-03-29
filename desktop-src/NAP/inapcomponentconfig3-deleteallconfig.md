---
title: Método INapComponentConfig3 DeleteAllConfig (NapCommon. h)
description: Lo implementan los validadores de mantenimiento del sistema (SHV) para proporcionar una manera de restablecer el almacén de SHV a su estado original después de la instalación.
ms.assetid: 7f079743-1c32-430d-a250-b49a96b99f14
keywords:
- Método DeleteAllConfig NAP
- Método DeleteAllConfig NAP, interfaz INapComponentConfig3
- Interfaz INapComponentConfig3 NAP, método DeleteAllConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteAllConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a766690114db20fb9be5cccbd4508f4565f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905126"
---
# <a name="inapcomponentconfig3deleteallconfig-method"></a>INapComponentConfig3::D método eleteAllConfig

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los validadores de mantenimiento del sistema (SHV) implementan el método **DeleteAllConfig** para proporcionar una manera de restablecer el almacén de SHV a su estado original después de la instalación. Se deben eliminar todos los datos de configuración excepto la configuración predeterminada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeleteAllConfig();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.



| Código devuelto                                                                           | Descripción                             |
|---------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl> | La operación se realizó correctamente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





