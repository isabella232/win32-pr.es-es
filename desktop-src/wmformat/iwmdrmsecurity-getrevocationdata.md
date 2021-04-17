---
title: Método IWMDRMSecurity GetRevocationData (wmdrmsdk. h)
description: El método GetRevocationData recupera una lista de revocación de certificados del almacén local.
ms.assetid: 218f4f3a-02bc-4b1d-9320-e35ed8cc3b11
keywords:
- Método GetRevocationData formato de Windows Media
- Método GetRevocationData formato de Windows Media, interfaz IWMDRMSecurity
- Interfaz IWMDRMSecurity formato de Windows Media, método GetRevocationData
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e9e0b428a3922f84141ef855d8468b79b3bb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670569"
---
# <a name="iwmdrmsecuritygetrevocationdata-method"></a>IWMDRMSecurity:: GetRevocationData (método)

El método **GetRevocationData** recupera una lista de revocación de certificados del almacén local.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRevocationData(
  [in]      REFGUID f_guidRevocationType,
  [out]     BYTE    *f_pbCRL,
  [in, out] DWORD   *f_pcbCRL
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*f \_ guidRevocationType* \[\]
</dt> <dd>

GUID que identifica el tipo de lista de revocación que se va a recuperar. Use una de las constantes de la tabla siguiente.



| Constante GUID                 | Descripción                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| \_aplicación REVOCATIONTYPE de WMDRM \_    | Especifica la lista de revocación de certificados de la aplicación.                           |
| \_dispositivo REVOCATIONTYPE \_ WMDRM | Especifica la lista de revocación de certificados de dispositivo.                                |
| \_CARDEA REVOCATIONTYPE \_ WMDRM | Especifica la lista de revocación de certificados de DRM de Windows Media para dispositivos de red. |



 

</dd> <dt>

*f \_ pbCRL* \[\]
</dt> <dd>

Búfer que recibe la lista de revocación. Establezca en **null** para obtener el tamaño de búfer necesario.

</dd> <dt>

*f \_ pcbCRL* \[ in, out\]
</dt> <dd>

Tamaño del búfer en bytes. Si *f \_ PbCRL* es **null**, este valor se establece en el tamaño de búfer necesario en la salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Revocación y renovación de componentes automatizados**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[**Interfaz IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> <dt>

[**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





