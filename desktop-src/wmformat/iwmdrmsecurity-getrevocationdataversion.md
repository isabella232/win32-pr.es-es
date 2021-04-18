---
title: Método IWMDRMSecurity GetRevocationDataVersion (wmdrmsdk. h)
description: El método GetRevocationDataVersion recupera el número de versión de una lista de revocación de certificados en el almacén local.
ms.assetid: 2fa13b38-02c2-4c81-938b-409cadca00fb
keywords:
- Método GetRevocationDataVersion formato de Windows Media
- Método GetRevocationDataVersion formato de Windows Media, interfaz IWMDRMSecurity
- Interfaz IWMDRMSecurity formato de Windows Media, método GetRevocationDataVersion
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationDataVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705f02622b7298134328b513aa038804995eb1c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670568"
---
# <a name="iwmdrmsecuritygetrevocationdataversion-method"></a>IWMDRMSecurity:: GetRevocationDataVersion (método)

El método **GetRevocationDataVersion** recupera el número de versión de una lista de revocación de certificados en el almacén local.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRevocationDataVersion(
  [in]  REFGUID   f_guidRevocationType,
  [out] ULONGLONG *f_pdwCRLVersion
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

*f \_ pdwCRLVersion* \[\]
</dt> <dd>

Variable que recibe el número de versión.

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

[**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[**Interfaz IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> <dt>

[**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





