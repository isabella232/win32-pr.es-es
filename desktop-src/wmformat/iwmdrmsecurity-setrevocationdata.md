---
title: Método IWMDRMSecurity SetRevocationData (Wmdrmsdk.h)
description: El método SetRevocationData establece una lista de revocación de certificados en el almacén local.
ms.assetid: 7e1c6d50-7a22-41b7-b29f-b1e5809a2097
keywords:
- Formato multimedia del método SetRevocationData
- Método SetRevocationData windows Media Format , interfaz IWMDRMSecurity
- IWMDRMSecurity interface windows Media Format , SetRevocationData method
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256244"
---
# <a name="iwmdrmsecuritysetrevocationdata-method"></a>IWMDRMSecurity::SetRevocationData (método)

El **método SetRevocationData** establece una lista de revocación de certificados en el almacén local.

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

*f \_ guidRevocationType* \[ en\]
</dt> <dd>

GUID que especifica el tipo de lista de revocación. Establezca en una de las constantes de la tabla siguiente.



| Constante GUID                 | Descripción                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| APLICACIÓN WMDRM \_ \_ REVOCATIONTYPE    | Especifica la lista de revocación de certificados de aplicación.                           |
| WMDRM \_ REVOCATIONTYPE \_ DEVICE | Especifica la lista de revocación de certificados de dispositivo.                                |
| WMDRM \_ REVOCATIONTYPE \_ CARDEA | Especifica la lista Windows revocación de certificados de DRM multimedia para dispositivos de red. |



 

</dd> <dt>

*f \_ pbCRL* \[ en\]
</dt> <dd>

Búfer que contiene la lista de revocación de certificados.

</dd> <dt>

*f \_ cbCRL* \[ en\]
</dt> <dd>

Tamaño del búfer, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[**Interfaz IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





