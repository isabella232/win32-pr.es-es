---
description: Rellena una matriz de punteros a las interfaces de IWiaItem2.
ms.assetid: 35fd5bdf-7e6c-431f-a9c6-62a86ee05f95
title: 'IEnumWiaItem2:: Next (método) (WIA. h)'
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
ms.openlocfilehash: 2e8800ead0c8f0abaddd0f055f31962d4d55d14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275641"
---
# <a name="ienumwiaitem2next-method"></a>IEnumWiaItem2:: Next (método)

Rellena una matriz de punteros a las interfaces de [**IWiaItem2**](-wia-iwiaitem2.md) .

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

*cElt* \[ de\]
</dt> <dd>

Tipo: **ULong**

Especifica el número de elementos de matriz de la matriz indicado por el parámetro *ppIWiaItem2* .

</dd> <dt>

*ppIWiaItem2* \[ enuncia\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Recibe la dirección de una matriz de punteros de interfaz [**IWiaItem2**](-wia-iwiaitem2.md) . **IEnumWiaItem2:: Next** rellena esta matriz con punteros de interfaz.

</dd> <dt>

*pcEltFetched* \[ in, out\]
</dt> <dd>

Tipo: **ULong \** _

En la salida, este parámetro recibe el número de punteros de interfaz almacenados realmente en la matriz indicada por el parámetro _ppIWiaItem2 *. Cuando se completa la enumeración, este parámetro contiene cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

El sistema en tiempo de ejecución de adquisición de imágenes de Windows (WIA) 2,0 representa dispositivos de hardware WIA 2,0 como un árbol jerárquico de objetos [**IWiaItem2**](-wia-iwiaitem2.md) . Las aplicaciones usan el método **IEnumWiaItem2:: Next** para obtener un puntero de interfaz **IWiaItem2** para cada elemento de la carpeta actual del árbol de objetos **IWiaItem2** de un dispositivo de hardware.

Para obtener la lista de punteros, la aplicación pasa una matriz de punteros de interfaz [**IWiaItem2**](-wia-iwiaitem2.md) que asigna. También pasa el número de elementos de matriz en el parámetro *cElt*. El método **IEnumWiaItem2:: Next** rellena la matriz con punteros a interfaces **IWiaItem2** .

Hasta que se complete el proceso de enumeración, el método **IEnumWiaItem2:: Next** devuelve S \_ correcto. Cada vez que lo hace, establece el valor al que apunta *pcEltFetched* en el número de elementos que insertó en la matriz. Cuando **IEnumWiaItem2:: Next** finaliza el proceso de enumeración de objetos [**IWiaItem2**](-wia-iwiaitem2.md) , devuelve S \_ false y establece la ubicación de memoria a la que apunta *pcEltFetched* en cero.

Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppIWiaItem2* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
