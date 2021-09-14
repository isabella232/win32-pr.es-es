---
title: Método CreateObject de IWMDRMProvider (Wmdrmsdk.h)
description: El método CreateObject recupera un puntero a una interfaz especificada y crea el objeto de implementación si es necesario.
ms.assetid: d408f7f3-9e49-4747-ac8f-d39db31d1240
keywords:
- Método CreateObject windows Media Format
- Método CreateObject windows Media Format , interfaz IWMDRMProvider
- IWMDRMProvider interface windows Media Format , CreateObject method
topic_type:
- apiref
api_name:
- IWMDRMProvider.CreateObject
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c0422138391b0d6f5e38fbc81fd5141bd3d8535
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247263"
---
# <a name="iwmdrmprovidercreateobject-method"></a>IWMDRMProvider::CreateObject (método)

El **método CreateObject** recupera un puntero a una interfaz especificada y crea el objeto de implementación si es necesario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateObject(
  [in]  REFIID riid,
  [out] void   **ppvObject
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*riid* \[ En\]
</dt> <dd>

Identificador de la interfaz que se va a crear. Establezca en uno de los valores siguientes.

-   IID \_ IWMDRMLicenseManagement
-   IID \_ IWMDRMLicenseQuery
-   IID \_ IWMDRMNetReceiver
-   IID \_ IWMDRMNetTransmitter
-   IID \_ IWMDRMSecurity

</dd> <dt>

*ppvObject* \[ out\]
</dt> <dd>

Dirección de un puntero que recibe la dirección de la interfaz solicitada.

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

[**IWMDRMProvider (interfaz)**](iwmdrmprovider.md)
</dt> <dt>

[**IWMDRMLicenseManagement (interfaz)**](iwmdrmlicensemanagement.md)
</dt> <dt>

[**IWMDRMLicenseQuery (interfaz)**](iwmdrmlicensequery.md)
</dt> <dt>

[**IWMDRMNetReceiver (interfaz)**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetTransmitter (interfaz)**](iwmdrmnettransmitter.md)
</dt> <dt>

[**IWMDRMSecurity (interfaz)**](iwmdrmsecurity.md)
</dt> </dl>

 

 





