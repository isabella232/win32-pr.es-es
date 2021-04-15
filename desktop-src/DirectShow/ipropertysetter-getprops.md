---
description: El método GetProps recupera las propiedades establecidas en este objeto, con sus valores correspondientes.
ms.assetid: 2a2ac262-f5a4-4bbe-9cd2-aa7c7d359917
title: 'IPropertySetter:: GetProps (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.GetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f512ce672cbbaca6556ad644f21c684130eb28e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690101"
---
# <a name="ipropertysettergetprops-method"></a>IPropertySetter:: GetProps (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetProps` método recupera las propiedades establecidas en este objeto, con sus valores correspondientes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetProps(
  [out] LONG         *pcParams,
  [out] DEXTER_PARAM **paParam,
  [out] DEXTER_VALUE **paValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcParams* \[ enuncia\]
</dt> <dd>

Recibe el número de estructuras devueltas en *param*.

</dd> <dt>

*param* \[ enuncia\]
</dt> <dd>

Dirección de un puntero a una matriz de estructuras de [**\_ parámetros de Dexterity**](dexter-param.md) .

</dd> <dt>

*Pavalue* \[ enuncia\]
</dt> <dd>

Dirección de un puntero a una matriz de estructuras de [**\_ valor de Dexterity**](dexter-value.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Para cada propiedad devuelta en *param*, el miembro **nvalores** indica el número de estructuras de [**\_ valor de Dexterity**](dexter-value.md) asociadas a la propiedad. Los pares se devuelven en orden de tiempo ascendente para cada propiedad.

Cuando haya terminado de usar las estructuras devueltas, llame a [**IPropertySetter:: FreeProps**](ipropertysetter-freeprops.md) para liberar los recursos asignados por este método.

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo recorrer en iteración todos los valores de una instancia del establecedor de propiedad:


```C++
IPropertySetter *pSetter = NULL;
// Get a valid IPropertySetter pointer (not shown).

DEXTER_PARAM *pParam;
DEXTER_VALUE *pValue;
LONG count;

hr = pSetter->GetProps(&count, &pParam, &pValue);

LONG num = 0;
for (LONG i = 0; i < count; i++)
{
    for (LONG j = 0; j < pParam[i].nValues; j++)
    {
        // pValue[num] is the next value in the sequence for pParam[i]
    }
    num += pParam[i].nValues;
}
```



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

 

 




