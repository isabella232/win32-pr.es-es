---
title: Método IMsTscAxEvents OnRequestContainerMinimize
description: Se llama cuando el usuario presiona el botón Minimizar en la barra de conexión en modo de pantalla completa. La activación de este evento es una solicitud que la aplicación contenedora se minimiza.
ms.assetid: fc052f9b-cf59-4d5a-ba39-571627b72f2a
ms.tgt_platform: multiple
keywords:
- Método OnRequestContainerMinimize Servicios de Escritorio remoto
- Método OnRequestContainerMinimize Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto método , OnRequestContainerMinimize
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestContainerMinimize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 344bd85d8d224a5901517c55c8e0a95c854ed246e74a9d0c8def1eebae515305
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125065"
---
# <a name="imstscaxeventsonrequestcontainerminimize-method"></a>Método IMsTscAxEvents::OnRequestContainerMinimize

Se llama cuando el usuario presiona el botón **Minimizar** en la barra de conexión en modo de pantalla completa. La activación de este evento es una solicitud que la aplicación contenedora se minimiza.

## <a name="syntax"></a>Sintaxis


```C++
void OnRequestContainerMinimize();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Solo se llamará a este método si el modo de pantalla completa controlada por contenedores está habilitado; vea [**IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) para obtener más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





