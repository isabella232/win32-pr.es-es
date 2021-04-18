---
title: Método IWMDRMLicenseManagement MonitorLicenseAcquisition (wmdrmsdk. h)
description: El método MonitorLicenseAcquisition inicia la supervisión de un proceso de adquisición de licencias.
ms.assetid: 725cd51a-a50b-4ff5-a880-7f551f6dba8f
keywords:
- Método MonitorLicenseAcquisition formato de Windows Media
- Método MonitorLicenseAcquisition formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método MonitorLicenseAcquisition
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.MonitorLicenseAcquisition
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25171d36a9d360f7c8eb77211c580c4f7676618f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718604"
---
# <a name="iwmdrmlicensemanagementmonitorlicenseacquisition-method"></a>IWMDRMLicenseManagement:: MonitorLicenseAcquisition (método)

El método **MonitorLicenseAcquisition** inicia la supervisión de un proceso de adquisición de licencias.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MonitorLicenseAcquisition(
  [in]  BSTR     bstrKID,
  [in]  BSTR     bstrHeader,
  [in]  BSTR     bstrActions,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrKID* \[ de\]
</dt> <dd>

IDENTIFICADOR de clave (KID) de la licencia adquirida.

</dd> <dt>

*bstrHeader* \[ de\]
</dt> <dd>

Encabezado de contenido usado en la llamada al método [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) .

</dd> <dt>

*bstrActions* \[ de\]
</dt> <dd>

Cadena que contiene las acciones solicitadas en la llamada al método **AcquireLicense** .

</dd> <dt>

*ppunkCancelationCookie* \[ enuncia\]
</dt> <dd>

Puntero que recibe un puntero a la interfaz **IUnknown** de un objeto que identifica esta llamada asincrónica. Este puntero de interfaz se puede usar para cancelar la llamada asincrónica llamando al método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





