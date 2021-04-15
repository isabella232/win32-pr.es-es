---
title: Método CreateObject de IWMDRMProvider (wmdrmsdk. h)
description: El método CreateObject recupera un puntero a una interfaz especificada y crea el objeto de implementación si es necesario.
ms.assetid: d408f7f3-9e49-4747-ac8f-d39db31d1240
keywords:
- Método CreateObject formato de Windows Media
- Método CreateObject formato de Windows Media, interfaz IWMDRMProvider
- Interfaz IWMDRMProvider formato de Windows Media, CreateObject (método)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649579"
---
# <a name="iwmdrmprovidercreateobject-method"></a>IWMDRMProvider:: CreateObject (método)

El método **CreateObject** recupera un puntero a una interfaz especificada y crea el objeto de implementación si es necesario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateObject(
  [in]  REFIID riid,
  [out] void   **ppvObject
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*riid* \[ de\]
</dt> <dd>

Identificador de la interfaz que se va a crear. Establezca en uno de los valores siguientes.

-   \_IWMDRMLICENSEMANAGEMENT IID
-   \_IWMDRMLICENSEQUERY IID
-   \_IWMDRMNETRECEIVER IID
-   \_IWMDRMNETTRANSMITTER IID
-   \_IWMDRMSECURITY IID

</dd> <dt>

*ppvObject* \[ enuncia\]
</dt> <dd>

Dirección de un puntero que recibe la dirección de la interfaz solicitada.

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

[**Interfaz IWMDRMProvider**](iwmdrmprovider.md)
</dt> <dt>

[**Interfaz IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> <dt>

[**Interfaz IWMDRMLicenseQuery**](iwmdrmlicensequery.md)
</dt> <dt>

[**Interfaz IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> <dt>

[**Interfaz IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> <dt>

[**Interfaz IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





