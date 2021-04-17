---
title: Método IWMDRMLicense GetLicense (wmdrmsdk. h)
description: El método GetLicense recupera la licencia como datos XML o XMR.
ms.assetid: 63317841-fd13-4e83-8b99-e3cab1405050
keywords:
- Método GetLicense formato de Windows Media
- Método GetLicense formato de Windows Media, interfaz IWMDRMLicense
- Interfaz IWMDRMLicense formato de Windows Media, método GetLicense
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
ms.openlocfilehash: 3d0692afb2ff127f9456e6da3c7546c67ae22ded
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708893"
---
# <a name="iwmdrmlicensegetlicense-method"></a>IWMDRMLicense:: GetLicense (método)

El método **GetLicense** recupera la licencia como datos XML o XMR.

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

*ppbLicense* \[ enuncia\]
</dt> <dd>

Recibe la licencia.

</dd> <dt>

*pcbLicense* \[ enuncia\]
</dt> <dd>

Recibe el tamaño de la licencia.

</dd> <dt>

*pdwLicenseType* \[ enuncia\]
</dt> <dd>

Recibe el tipo de la licencia devuelta. Este valor se establece en una de las constantes de la tabla siguiente.



| Constante                  | Descripción                            |
|---------------------------|----------------------------------------|
| tipo de licencia de WMDRM \_ \_ \_ XML | La licencia recuperada tiene el formato XML. |
| tipo de licencia de WMDRM \_ \_ \_ XMR | La licencia recuperada tiene el formato XMR. |



 

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

[**GetLicenseProperty**](iwmdrmlicense-getlicenseproperty.md)
</dt> <dt>

[**Interfaz IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





