---
description: El método CloneProps clona un conjunto de propiedades de este establecedor de propiedad y los agrega a un nuevo establecedor de propiedad.
ms.assetid: dee93e41-2925-4b4b-b5b2-7cfd6ea10e05
title: 'IPropertySetter:: CloneProps (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.CloneProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9954b98085ba2de9eac6bc62bf784732448f613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690102"
---
# <a name="ipropertysettercloneprops-method"></a>IPropertySetter:: CloneProps (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `CloneProps` método clona un conjunto de propiedades de este establecedor de propiedad y los agrega a un nuevo establecedor de propiedad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CloneProps(
  [out] IPropertySetter **ppSetter,
  [in]  REFERENCE_TIME  rtStart,
  [in]  REFERENCE_TIME  rtStop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppSetter* \[ enuncia\]
</dt> <dd>

Recibe un puntero a la interfaz **IPropertySetter** del nuevo establecedor de propiedad.

</dd> <dt>

*rtStart* \[ de\]
</dt> <dd>

Hora de inicio del intervalo de valores que se va a clonar, en unidades de 100-nanosegundos.

</dd> <dt>

*rtStop* \[ de\]
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Solo se clonan los valores que se encuentran después de la hora de inicio especificada. Las horas de los valores clonados se ajustan en relación con la hora de inicio. Por ejemplo, si *rtStart* es 20 millones (2 segundos), se clona un valor en el tiempo 30 millones (3 segundos) con la hora 10 millones (1 segundo). Por último, a cada propiedad clonada se le asigna un valor inicial igual al valor de la propiedad original en la hora de inicio (correctamente interpolada si es necesario). En efecto, los datos de la propiedad se dividen a la hora de inicio especificada.

Si el método se ejecuta correctamente, la interfaz [**IPropertySetter**](ipropertysetter.md) que devuelve tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando termine de usarla.

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

 

 




