---
title: Método IWMDRMSecurity PerformSecurityUpdate (Wmdrmsdk.h)
description: El método PerformSecurityUpdate inicia una actualización de seguridad para el subsistema DRM en el equipo local.
ms.assetid: e450a1e3-6024-4c00-9978-fbc88fde2101
keywords:
- Formato multimedia de windows del método PerformSecurityUpdate
- Método PerformSecurityUpdate windows Media Format , IWMDRMSecurity (interfaz)
- IWMDRMSecurity interface windows Media Format , PerformSecurityUpdate method
topic_type:
- apiref
api_name:
- IWMDRMSecurity.PerformSecurityUpdate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34a1e92edd279655737a2e8f3b7ce4e77e27fd5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360218"
---
# <a name="iwmdrmsecurityperformsecurityupdate-method"></a>IWMDRMSecurity::P erformSecurityUpdate (método)

El **método PerformSecurityUpdate** inicia una actualización de seguridad para el subsistema DRM en el equipo local.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PerformSecurityUpdate(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Opción de actualización expresada como una de las marcas siguientes.



| Marca                                          | Descripción                                                                                     |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------|
| WMDRM \_ SECURITY \_ PERFORM \_ INDIV               | Hace que el componente DRM se individualiza solo si la versión del cliente no está actualizada. |
| SEGURIDAD DE WMDRM \_ REALIZA LA ACTUALIZACIÓN DE \_ \_ \_ REVOCACIÓN | Hace que las listas de revocación del equipo cliente se actualicen.                               |
| WMDRM \_ SECURITY \_ PERFORM \_ FORCE \_ INDIV        | Hace que el componente DRM se individualiza incluso si la versión del cliente está actualizada.  |



 

</dd> <dt>

*piqueCancelationCookie* \[ out\]
</dt> <dd>

Dirección de una variable que recibe un puntero a un objeto que se puede usar para cancelar esta operación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método se ejecuta de forma asincrónica. Devuelve inmediatamente después de llamar a y, a continuación, genera eventos en función de la marca establecida en el *parámetro dwFlags.*

Para la individualización (marca establecida en WMDRM SECURITY PERFORM INDIV o WMDRM SECURITY PERFORM FORCE INDIV), se genera una serie de eventos \_ \_ \_ \_ \_ \_ \_ **MEWMDRMIndividualizationProgress** seguidos de un evento **MEWMDRMIndividualizationCompleted** cuando se completa el procesamiento. El valor de cada uno de los eventos **MEWMDRMIndividualizationProgress obtenidos** mediante una llamada a **IMFMediaEvent::GetValue** es un **puntero IUnknown.** Puede llamar al **método QueryInterface** de la interfaz **IUnknown** recuperada para obtener una instancia de la interfaz [**IWMDRMIndividualizationStatus.**](iwmdrmindividualizationstatus.md)

Para actualizar las listas de revocación (marca establecida en WMDRM SECURITY PERFORM REVOCATION REFRESH), se genera un evento \_ \_ \_ \_ **MEWMDRMREvocationDownloadCompleted** cuando se completa el procesamiento.

> [!Note]  
> Cuando **PerformSecurityUpdate** completa la individualización, los únicos objetos existentes que reflejarán el nuevo estado individualizado son los que heredan de **IWMDRMSecurity**. No se actualizarán todos los demás objetos existentes. Debe liberar y volver a crear cualquier otro objeto para que refleje el nuevo estado individualizado.

 

Para obtener más información sobre el uso de los métodos asincrónicos de Windows MEDIA DRM Client Extended API, vea [Using the Media Foundation Event Model](using-the-media-foundation-model.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Revocación y renovación automatizadas de componentes**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**Ejemplo de individualización de DRM**](drm-individualization-example.md)
</dt> <dt>

[**IWMDRMSecurity (interfaz)**](iwmdrmsecurity.md)
</dt> <dt>

[**Realización de la individualización de DRM**](performing-drm-individualization.md)
</dt> </dl>

 

 





