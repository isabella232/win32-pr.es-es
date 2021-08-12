---
title: Método INapComponentConfig3 DeleteAllConfig (NapCommon.h)
description: Se implementa mediante validadores de estado del sistema (SHV) para proporcionar una manera de restablecer el almacén shv a su estado original después de la instalación.
ms.assetid: 7f079743-1c32-430d-a250-b49a96b99f14
keywords:
- Método Nap de DeleteAllConfig
- Método DeleteAllConfig NAP , interfaz INapComponentConfig3
- Nap de interfaz INapComponentConfig3, método DeleteAllConfig
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
ms.openlocfilehash: 05b2a81a33dfb659c3398c8c853132244d088b7fa65bd4bb0317869e13b85abf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621744"
---
# <a name="inapcomponentconfig3deleteallconfig-method"></a>INapComponentConfig3::D eleteAllConfig (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los validadores de estado del sistema (SHV) implementan el método **DeleteAllConfig** para proporcionar una manera de restablecer el almacén de SHV a su estado original después de la instalación. Se deben eliminar todos los datos de configuración excepto la configuración predeterminada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeleteAllConfig();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error según el resultado de esta operación.



| Código devuelto                                                                           | Descripción                             |
|---------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl> | La operación se realizó correctamente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                  |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





