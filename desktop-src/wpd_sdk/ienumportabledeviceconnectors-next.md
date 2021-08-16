---
description: Recupera el siguiente objeto IPortableDeviceConnector en la secuencia de enumeración.
ms.assetid: 5aed563a-5ecc-49c0-8a0c-622405453896
title: Método IEnumPortableDeviceConnectors::Next (Devpkey.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Next
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 868f13f220dbd5d5867e5ee2bbb54c1ef946e267d87e9ea0aa625108b945d537
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697300"
---
# <a name="ienumportabledeviceconnectorsnext-method"></a>IEnumPortableDeviceConnectors::Next (Método)

El **método Next** recupera los siguientes objetos [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) en la secuencia de enumeración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Next(
  [in]      UINT32                   cRequested,
  [out]     IPortableDeviceConnector **pConnectors,
  [in, out] UINT32                   *pcFetched
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cRequested* \[ En\]
</dt> <dd>

Número de dispositivos solicitados. Este valor también indica el número de elementos de la matriz asignada por el autor de la llamada especificada por el *parámetro pConnectors.*

</dd> <dt>

*pConnectors* \[ out\]
</dt> <dd>

Matriz de [**punteros IPortableDeviceConnector,**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) cada uno de los que especifica un MTP Bluetooth dispositivo. El autor de la llamada debe asignar una matriz de punteros **IPortableDeviceConnector,** con la longitud de matriz especificada por *el parámetro cRequested.* Si la devolución es correcta, el autor de la llamada debe liberar tanto la matriz como los punteros devueltos. Las **interfaces IPortableDeviceConnector** se liberan mediante una llamada **al método IUnknown::Release.**

</dd> <dt>

*pcFetched* \[ in, out\]
</dt> <dd>

Número de interfaces [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) que se recuperan realmente. Si no se recupera ninguna interfaz **IPortableDeviceConnector** y el valor devuelto es **S \_ FALSE,** no hay más interfaces **IPortableDeviceConnector** para enumerar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                             | Descripción                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | El método se ha llevado a cabo de forma correcta.<br/>                                 |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | No hay más dispositivos MTP Bluetooth enumerar.<br/> |



 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso de este método para enumerar los dispositivos MTP/Bluetooth emparejados y para enviar una solicitud de conexión asincrónica a cada uno de ellos.


```C++
IEnumPortableDeviceConnectors* pEnum = NULL;
    HRESULT hrEnum = S_OK;
 HRESULT hr = CoCreateInstance(CLSID_EnumBthMtpConnectors, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pEnum));
    if (SUCCEEDED(hr))
{
  while (S_OK == hrEnum)
    {
       UINT32  uFetched        = 0;
       LPWSTR  wszDevicePnPID  = NULL;
       IPortableDeviceConnector* pDevice = NULL;
       hrEnum = pEnum->Next(1, &spDevice, &uFetched);
       if (hrEnum == S_OK && uFetched == 1)
        {
          // Send an asynchronous connect request.  
          hr = pDevice ->Connect(NULL);
          // Release the device when done
          pDevice->Release();
          pDevice = NULL;
        }
     }  // while S_OK == hrEnum
  // Release the enumerator when done
    if (pEnum)
    {
     pEnum->Release();
     pEnum = NULL;
   }
    }
       
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                                                                             |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi.idl</dt> </dl>                                                                |
| Biblioteca<br/>                  | <dl> <dt>PortableDeviceGuids.lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




