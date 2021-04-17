---
title: Método IWMDRMSecurity SetRevocationData (wmdrmsdk. h)
description: El método SetRevocationData establece una lista de revocación de certificados en el almacén local.
ms.assetid: 7e1c6d50-7a22-41b7-b29f-b1e5809a2097
keywords:
- Método SetRevocationData formato de Windows Media
- Método SetRevocationData formato de Windows Media, interfaz IWMDRMSecurity
- Interfaz IWMDRMSecurity formato de Windows Media, método SetRevocationData
topic_type:
- apiref
api_name:
- IWMDRMSecurity.SetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3ece5a9285420261add123a61d0b7123896e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670567"
---
# <a name="iwmdrmsecuritysetrevocationdata-method"></a>IWMDRMSecurity:: SetRevocationData (método)

El método **SetRevocationData** establece una lista de revocación de certificados en el almacén local.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetRevocationData(
  [in] REFGUID f_guidRevocationType,
  [in] BYTE    *f_pbCRL,
  [in] DWORD   f_cbCRL
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*f \_ guidRevocationType* \[\]
</dt> <dd>

GUID que especifica el tipo de lista de revocación. Establezca en una de las constantes de la tabla siguiente.



| Constante GUID                 | Descripción                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| \_aplicación REVOCATIONTYPE de WMDRM \_    | Especifica la lista de revocación de certificados de la aplicación.                           |
| \_dispositivo REVOCATIONTYPE \_ WMDRM | Especifica la lista de revocación de certificados de dispositivo.                                |
| \_CARDEA REVOCATIONTYPE \_ WMDRM | Especifica la lista de revocación de certificados de DRM de Windows Media para dispositivos de red. |



 

</dd> <dt>

*f \_ pbCRL* \[\]
</dt> <dd>

Búfer que contiene la lista de revocación de certificados.

</dd> <dt>

*f \_ cbCRL* \[\]
</dt> <dd>

Tamaño del búfer, en bytes.

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

[**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[**Interfaz IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





