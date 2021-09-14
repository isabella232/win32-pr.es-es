---
title: Método IWMDRMSecurity GetRevocationData (Wmdrmsdk.h)
description: El método GetRevocationData recupera una lista de revocación de certificados del almacén local.
ms.assetid: 218f4f3a-02bc-4b1d-9320-e35ed8cc3b11
keywords:
- Método GetRevocationData windows Media Format
- Método GetRevocationData windows Media Format , interfaz IWMDRMSecurity
- IWMDRMSecurity interface windows Media Format , GetRevocationData method
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256262"
---
# <a name="iwmdrmsecuritygetrevocationdata-method"></a>IWMDRMSecurity::GetRevocationData (método)

El **método GetRevocationData** recupera una lista de revocación de certificados del almacén local.

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

*f \_ guidRevocationType* \[ en\]
</dt> <dd>

GUID que identifica el tipo de lista de revocación que se recuperará. Use una de las constantes de la tabla siguiente.



| Constante GUID                 | Descripción                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| APLICACIÓN WMDRM \_ \_ REVOCATIONTYPE    | Especifica la lista de revocación de certificados de aplicación.                           |
| DISPOSITIVO WMDRM \_ \_ REVOCATIONTYPE | Especifica la lista de revocación de certificados de dispositivo.                                |
| WMDRM \_ REVOCATIONTYPE \_ CARDEA | Especifica la lista de revocación de Windows DRM multimedia para dispositivos de red. |



 

</dd> <dt>

*f \_ pbCRL* \[ out\]
</dt> <dd>

Búfer que recibe la lista de revocación. Establezca en **NULL** para obtener el tamaño de búfer necesario.

</dd> <dt>

*f \_ pwCRL* \[ in, out\]
</dt> <dd>

Tamaño del búfer en bytes. Si *f \_ pbCRL* es **NULL,** este valor se establece en el tamaño de búfer necesario en la salida.

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

[**Revocación y renovación automatizadas de componentes**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[**IWMDRMSecurity (interfaz)**](iwmdrmsecurity.md)
</dt> <dt>

[**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





