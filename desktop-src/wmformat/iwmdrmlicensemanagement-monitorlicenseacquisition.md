---
title: Método IWMDRMLicenseManagement MonitorLicenseAcquisition (Wmdrmsdk.h)
description: El método MonitorLicenseAcquisition inicia la supervisión de un proceso de adquisición de licencias.
ms.assetid: 725cd51a-a50b-4ff5-a880-7f551f6dba8f
keywords:
- Método MonitorLicenseAcquisition windows Media Format
- Método MonitorLicenseAcquisition windows Media Format , IWMDRMLicenseManagement (interfaz)
- IWMDRMLicenseManagement interface windows Media Format , MonitorLicenseAcquisition method
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
ms.openlocfilehash: b7ab3188425decca614ae104989fdc2f07930ac0de463e492be630a3fb54556e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027583"
---
# <a name="iwmdrmlicensemanagementmonitorlicenseacquisition-method"></a>IWMDRMLicenseManagement::MonitorLicenseAcquisition (método)

El **método MonitorLicenseAcquisition** inicia la supervisión de un proceso de adquisición de licencias.

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

*bstrKID* \[ En\]
</dt> <dd>

Identificador de clave (KID) de la licencia que se va a adquirir.

</dd> <dt>

*bstrHeader* \[ En\]
</dt> <dd>

Encabezado de contenido que se usó en la llamada al [**método AcquireLicense.**](iwmdrmlicensemanagement-acquirelicense.md)

</dd> <dt>

*bstrActions* \[ En\]
</dt> <dd>

Cadena que contiene las acciones solicitadas en la llamada al **método AcquireLicense.**

</dd> <dt>

*piqueCancelationCookie* \[ out\]
</dt> <dd>

Puntero que recibe un puntero a la **interfaz IUnknown** de un objeto que identifica esta llamada asincrónica. Este puntero de interfaz se puede usar para cancelar la llamada asincrónica llamando al método [**IWMDRMEventGenerator::CancelAsyncOperation.**](iwmdrmeventgenerator-cancelasyncoperation.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDRMLicenseManagement (interfaz)**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





