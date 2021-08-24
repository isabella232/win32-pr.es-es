---
description: Rellena una matriz de punteros a interfaces IWiaItem2.
ms.assetid: 35fd5bdf-7e6c-431f-a9c6-62a86ee05f95
title: Método IEnumWiaItem2::Next (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Next
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: cf884375f504bb801bcebcaad3f75b23c5f82956ce3a1d45dd5a50bfa5f8e53c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451145"
---
# <a name="ienumwiaitem2next-method"></a>IEnumWiaItem2::Next (Método)

Rellena una matriz de punteros a [**interfaces IWiaItem2.**](-wia-iwiaitem2.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Next(
  [in]      ULONG     cElt,
  [out]     IWiaItem2 **ppIWiaItem2,
  [in, out] ULONG     *pcEltFetched
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cElt* \[ En\]
</dt> <dd>

Tipo: **ULONG**

Especifica el número de elementos de matriz de la matriz indicado por el *parámetro ppIWiaItem2.*

</dd> <dt>

*ppIWiaItem2* \[ out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Recibe la dirección de una matriz de punteros de interfaz [**IWiaItem2.**](-wia-iwiaitem2.md) **IEnumWiaItem2::Next** rellena esta matriz con punteros de interfaz.

</dd> <dt>

*pcEltFetched* \[ in, out\]
</dt> <dd>

Tipo: **ULONG \***

En la salida, este parámetro recibe el número de punteros de interfaz almacenados realmente en la matriz indicada por el *parámetro ppIWiaItem2.* Una vez completada la enumeración, este parámetro contiene cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

El sistema de tiempo de ejecución Windows Image Acquisition (WIA) 2.0 representa los dispositivos de hardware WIA 2.0 como un árbol jerárquico de objetos [**IWiaItem2.**](-wia-iwiaitem2.md) Las aplicaciones usan el método **IEnumWiaItem2::Next** para obtener un puntero de interfaz **IWiaItem2** para cada elemento de la carpeta actual del árbol de objetos **IWiaItem2** de un dispositivo de hardware.

Para obtener la lista de punteros, la aplicación pasa una matriz de punteros de interfaz [**IWiaItem2**](-wia-iwiaitem2.md) que asigna. También pasa el número de elementos de matriz en el parámetro *cElt*. El **método IEnumWiaItem2::Next** rellena la matriz con punteros a interfaces **IWiaItem2.**

Hasta que se complete el proceso de enumeración, el **método IEnumWiaItem2::Next** devuelve S \_ OK. Cada vez que lo hace, establece el valor al que apunta *pcEltFetched* en el número de elementos que insertó en la matriz. Cuando **IEnumWiaItem2::Next** finaliza el proceso de enumeración de objetos [**IWiaItem2,**](-wia-iwiaitem2.md) devuelve S FALSE y establece la ubicación de memoria a la que \_ apunta *pcEltFetched* en cero.

Las aplicaciones deben llamar [al método IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del *parámetro ppIWiaItem2.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
