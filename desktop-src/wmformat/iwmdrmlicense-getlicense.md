---
title: Método IWMDRMLicense GetLicense (Wmdrmsdk.h)
description: El método GetLicense recupera la licencia como datos XML o XMR.
ms.assetid: 63317841-fd13-4e83-8b99-e3cab1405050
keywords:
- Método GetLicense windows Media Format
- Método GetLicense windows Media Format , interfaz IWMDRMLicense
- IWMDRMLicense interface windows Media Format , GetLicense (método)
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b303c3280b42858bb319bb49baa209c1f99cdac819a719743db403bfdc08ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585405"
---
# <a name="iwmdrmlicensegetlicense-method"></a>IWMDRMLicense::GetLicense (método)

El **método GetLicense** recupera la licencia como datos XML o XMR.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetLicense(
  [out] BYTE  **ppbLicense,
  [out] DWORD *pcbLicense,
  [out] DWORD *pdwLicenseType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppbLicense* \[ out\]
</dt> <dd>

Recibe la licencia.

</dd> <dt>

*licencia de la licencia* \[ out\]
</dt> <dd>

Recibe el tamaño de la licencia.

</dd> <dt>

*pdwLicenseType* \[ out\]
</dt> <dd>

Recibe el tipo de la licencia devuelta. Este valor se establece en una de las constantes de la tabla siguiente.



| Constante                  | Descripción                            |
|---------------------------|----------------------------------------|
| XML DE TIPO \_ DE LICENCIA \_ \_ WMDRM | La licencia recuperada tiene el formato XML. |
| TIPO DE LICENCIA DE WMDRM \_ \_ \_ XMR | La licencia recuperada tiene el formato XMR. |



 

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

[**GetLicenseProperty**](iwmdrmlicense-getlicenseproperty.md)
</dt> <dt>

[**IWMDRMLicense (Interfaz)**](iwmdrmlicense.md)
</dt> </dl>

 

 





