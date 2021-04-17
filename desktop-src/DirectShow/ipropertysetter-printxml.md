---
description: El método PrintXML convierte los datos de propiedad en una cadena XML.
ms.assetid: 24638489-b5ed-4bdd-b40e-6d61c0db1533
title: IPropertySetter::P método rintXML (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.PrintXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f31d36e8642cb669f5e365d6ffe25b538268bd1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680494"
---
# <a name="ipropertysetterprintxml-method"></a>IPropertySetter::P método rintXML

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `PrintXML` método convierte los datos de propiedad en una cadena XML.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PrintXML(
  [out] char *pszXML,
  [in]  int  cbXML,
  [out] int  *pcbPrinted,
  [in]  int  indent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszXML* \[ enuncia\]
</dt> <dd>

Puntero a un búfer que recibe la cadena XML.

</dd> <dt>

*cbXML* \[ de\]
</dt> <dd>

Tamaño del búfer al que apunta *pszXML*, en bytes.

</dd> <dt>

*pcbPrinted* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe la longitud de la cadena XML. Puede ser **null**.

</dd> <dt>

*aplicar sangría* \[ de\]
</dt> <dd>

Número de niveles de sangría para la etiqueta más externa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto si se realiza correctamente. De lo contrario, devuelve un valor **HRESULT** que indica la causa del error. Si la cadena XML es más larga que el búfer, el método devuelve E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

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

 

 




