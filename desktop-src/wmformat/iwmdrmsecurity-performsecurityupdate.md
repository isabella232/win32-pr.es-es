---
title: Método IWMDRMSecurity PerformSecurityUpdate (wmdrmsdk. h)
description: El método PerformSecurityUpdate inicia una actualización de seguridad para el subsistema DRM en el equipo local.
ms.assetid: e450a1e3-6024-4c00-9978-fbc88fde2101
keywords:
- Método PerformSecurityUpdate formato de Windows Media
- Método PerformSecurityUpdate formato de Windows Media, interfaz IWMDRMSecurity
- Interfaz IWMDRMSecurity formato de Windows Media, método PerformSecurityUpdate
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708263"
---
# <a name="iwmdrmsecurityperformsecurityupdate-method"></a>IWMDRMSecurity::P método erformSecurityUpdate

El método **PerformSecurityUpdate** inicia una actualización de seguridad para el subsistema DRM en el equipo local.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PerformSecurityUpdate(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Opción de actualización expresada como una de las marcas siguientes.



| Marca                                          | Descripción                                                                                     |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------|
| la \_ seguridad de WMDRM \_ realiza \_ indiv               | Hace que el componente DRM se sutaque solo si la versión del cliente no está actualizada. |
| \_actualización de \_ la \_ revocación \_ de seguridad de WMDRM | Hace que se actualicen las listas de revocación en el equipo cliente.                               |
| seguridad de WMDRM, \_ \_ \_ forzar \_ indiv        | Hace que el componente DRM se Suscríbase incluso si la versión del cliente está actualizada.  |



 

</dd> <dt>

*ppunkCancelationCookie* \[ enuncia\]
</dt> <dd>

Dirección de una variable que recibe un puntero a un objeto que se puede usar para cancelar esta operación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método se ejecuta de forma asincrónica. Vuelve inmediatamente después de llamarse a y, a continuación, genera eventos en función de la marca establecida en el parámetro *dwFlags* .

En el caso de la individualización (la marca establecida en seguridad de WMDRM \_ \_ realiza \_ indiv o WMDRM \_ Security \_ realice \_ Force \_ indiv), se genera una serie de eventos **MEWMDRMIndividualizationProgress** seguidos de un evento **MEWMDRMIndividualizationCompleted** cuando se completa el procesamiento. El valor de cada uno de los eventos **MEWMDRMIndividualizationProgress** obtenidos mediante la llamada a **IMFMediaEvent:: GetValue** es un puntero **IUnknown** . Puede llamar al método **QueryInterface** de la interfaz **IUnknown** recuperada para obtener una instancia de la interfaz [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) .

Para actualizar las listas de revocación (marca establecida en seguridad de WMDRM, \_ \_ realizar la actualización de \_ revocación \_ ), se genera un evento **MEWMDRMREvocationDownloadCompleted** cuando se completa el procesamiento.

> [!Note]  
> Cuando **PerformSecurityUpdate** complete la individualización, los únicos objetos existentes que reflejen el nuevo estado individualizado son los que heredan de **IWMDRMSecurity**. No se actualizarán todos los demás objetos existentes. Debe liberar y volver a crear los demás objetos para que reflejen el nuevo estado de forma individual.

 

Para obtener más información sobre el uso de los métodos asincrónicos de las API extendidas del cliente DRM de Windows Media, vea [usar el modelo de eventos de Media Foundation](using-the-media-foundation-model.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Revocación y renovación de componentes automatizados**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**Ejemplo de individualización de DRM**](drm-individualization-example.md)
</dt> <dt>

[**Interfaz IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> <dt>

[**Realización de una individualización DRM**](performing-drm-individualization.md)
</dt> </dl>

 

 





