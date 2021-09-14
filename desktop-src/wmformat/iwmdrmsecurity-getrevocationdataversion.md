---
title: Método IWMDRMSecurity GetRevocationDataVersion (Wmdrmsdk.h)
description: El método GetRevocationDataVersion recupera el número de versión de una lista de revocación de certificados en el almacén local.
ms.assetid: 2fa13b38-02c2-4c81-938b-409cadca00fb
keywords:
- Formato multimedia de windows del método GetRevocationDataVersion
- Método GetRevocationDataVersion windows Media Format , interfaz IWMDRMSecurity
- IWMDRMSecurity interface windows Media Format , GetRevocationDataVersion method
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256256"
---
# <a name="iwmdrmsecuritygetrevocationdataversion-method"></a>IWMDRMSecurity::GetRevocationDataVersion (método)

El **método GetRevocationDataVersion** recupera el número de versión de una lista de revocación de certificados en el almacén local.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRevocationDataVersion(
  [in]  REFGUID   f_guidRevocationType,
  [out] ULONGLONG *f_pdwCRLVersion
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
| WMDRM \_ REVOCATIONTYPE \_ CARDEA | Especifica la lista de revocación de Windows drm multimedia para dispositivos de red. |



 

</dd> <dt>

*f \_ pdwCRLVersion* \[ out\]
</dt> <dd>

Variable que recibe el número de versión.

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

[**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[**Interfaz IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> <dt>

[**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





