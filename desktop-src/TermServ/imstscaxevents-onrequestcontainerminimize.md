---
title: IMsTscAxEvents OnRequestContainerMinimize, método
description: Se llama cuando el usuario presiona el botón minimizar en la barra de conexión en el modo de pantalla completa. La activación de este evento es una solicitud que la aplicación contenedora se minimiza por sí misma.
ms.assetid: fc052f9b-cf59-4d5a-ba39-571627b72f2a
ms.tgt_platform: multiple
keywords:
- Método OnRequestContainerMinimize Servicios de Escritorio remoto
- Método OnRequestContainerMinimize Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnRequestContainerMinimize
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
ms.openlocfilehash: 85387e3b156eed29dc7068eac84280be521a934e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422423"
---
# <a name="imstscaxeventsonrequestcontainerminimize-method"></a>IMsTscAxEvents:: OnRequestContainerMinimize (método)

Se llama cuando el usuario presiona el botón **minimizar** en la barra de conexión en el modo de pantalla completa. La activación de este evento es una solicitud que la aplicación contenedora se minimiza por sí misma.

## <a name="syntax"></a>Sintaxis


```C++
void OnRequestContainerMinimize();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Solo se llamará a este método si está habilitado el modo de pantalla completa controlado por contenedores; consulte [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) para obtener más información.

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

 

 





