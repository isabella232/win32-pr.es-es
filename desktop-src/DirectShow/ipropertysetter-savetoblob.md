---
description: El método SaveToBlob guarda los datos de la propiedad en un formato de persistencia.
ms.assetid: 48201192-abda-484e-bdb3-442aca52b2bf
title: 'IPropertySetter:: SaveToBlob (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SaveToBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 97e248ebf741b45e73c82b17eee4181b1f19ac35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680492"
---
# <a name="ipropertysettersavetoblob-method"></a>IPropertySetter:: SaveToBlob (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SaveToBlob` método guarda los datos de la propiedad en un formato de persistencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SaveToBlob(
  [out] LONG *pcSize,
  [out] BYTE **ppb
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcSize* \[ enuncia\]
</dt> <dd>

Recibe el tamaño de los datos, en bytes.

</dd> <dt>

*ppb* \[ enuncia\]
</dt> <dd>

Recibe un puntero a una matriz de bytes que recibe los datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

El método asigna memoria para la matriz de bytes. El autor de la llamada debe liberarlo mediante la función **CoTaskMemFree** .

Todos los valores y nombres de propiedad se truncan hasta 40 caracteres de longitud. Por esta razón, XML es el formato de persistencia preferido. Consulte la [**interfaz IXml2Dex**](ixml2dex.md).

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




