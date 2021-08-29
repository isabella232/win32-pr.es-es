---
description: El método GetProps recupera las propiedades establecidas en este objeto, con sus valores correspondientes.
ms.assetid: 2a2ac262-f5a4-4bbe-9cd2-aa7c7d359917
title: Método IPropertySetter::GetProps (Qedit.h)
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
ms.openlocfilehash: 10a2f1cd8be327a288d37ddee8acf3a7f02433897c938bebaf7ad2aa3af24105
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131035"
---
# <a name="ipropertysettergetprops-method"></a>IPropertySetter::GetProps (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

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

*pcParams* \[ out\]
</dt> <dd>

Recibe el número de estructuras devueltas *en paParam*.

</dd> <dt>

*paParam* \[ out\]
</dt> <dd>

Dirección de un puntero a una matriz de [**estructuras \_ PARAM DESTRO.**](dexter-param.md)

</dd> <dt>

*paValue* \[ out\]
</dt> <dd>

Dirección de un puntero a una matriz de [**estructuras VALUE \_ DE COLOR.**](dexter-value.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Para cada propiedad devuelta en *paParam*, el **miembro nValues** indica el número de estructuras [**DE \_ VALOR DE PRECIO**](dexter-value.md) asociadas a la propiedad. Los pares se devuelven en orden de tiempo ascendente para cada propiedad.

Cuando haya terminado de usar las estructuras devueltas, llame a [**IPropertySetter::FreeProps**](ipropertysetter-freeprops.md) para liberar los recursos asignados por este método.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo recorrer en iteración todos los valores de una instancia del setter de propiedad:


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
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPropertySetter (interfaz)**](ipropertysetter.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




