---
title: Método IWMDRMLicense GetInclusionList (Wmdrmsdk.h)
description: El método GetInclusionList recupera toda la lista de inclusión para la cadena de licencias o licencias actual.
ms.assetid: a3cb70c5-7d20-413c-aeb8-66c9233b384e
keywords:
- Método GetInclusionList windows Media Format
- Método GetInclusionList windows Media Format , interfaz IWMDRMLicense
- IWMDRMLicense interfaz windows Media Format , Método GetInclusionList
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetInclusionList
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f0d2837a4bb84c07214cce3e4fbc3d4d96b9583
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466484"
---
# <a name="iwmdrmlicensegetinclusionlist-method"></a>IWMDRMLicense::GetInclusionList (método)

El **método GetInclusionList** recupera toda la lista de inclusión para la cadena de licencias o licencias actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetInclusionList(
  [out] GUID  **ppGuids,
  [out] DWORD *pcGuids
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppGuids* \[ out\]
</dt> <dd>

Recibe una matriz de GUID que identifican las tecnologías incluidas.

</dd> <dt>

*pcGuids* \[ out\]
</dt> <dd>

Recibe el número de elementos de la matriz *ppGuids.* La matriz se asigna mediante **CoTaskMemAlloc**. Cuando termine con la lista, libere la memoria mediante una llamada **a CoTaskMemFree**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

El emisor de la licencia puede especificar otros sistemas de protección a los que se puede convertir el contenido cifrado. La lista de GUID recuperada por este método identifica los sistemas de protección permitidos. Al entrar en un contrato de licencia con Microsoft para obtener la biblioteca de código auxiliar, recibirá una lista de los sistemas de protección admitidos actualmente y los GUID que se usan para identificarlos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Listas explícitas de autorización e inclusión**](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[**Interfaz IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





