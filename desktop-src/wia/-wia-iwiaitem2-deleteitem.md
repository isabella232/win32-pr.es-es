---
description: Quita el objeto IWiaItem2 actual del árbol de objetos del dispositivo.
ms.assetid: 247eb36f-3e5c-4030-8334-1a4028b3eb44
title: IWiaItem2::D método eleteItem (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeleteItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: ef6a4204b591f06811f0941ca0ceed72b76151db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715196"
---
# <a name="iwiaitem2deleteitem-method"></a>IWiaItem2::D método eleteItem

Quita el objeto [**IWiaItem2**](-wia-iwiaitem2.md) actual del árbol de objetos del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeleteItem(
  [in] LONG lFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

Actualmente no se usa. Debe establecerse como cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

El sistema en tiempo de ejecución de adquisición de imágenes de Windows (WIA) 2,0 representa cada dispositivo de hardware WIA 2,0 conectado al equipo del usuario como un árbol jerárquico de objetos [**IWiaItem2**](-wia-iwiaitem2.md) . Un determinado dispositivo WIA 2,0 puede permitir o no que las aplicaciones eliminen objetos **IWiaItem2** de su árbol. Los elementos que tienen elementos secundarios no se pueden eliminar. La interfaz [**IEnumWIA \_ dev \_ caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) debe usarse para consultar el dispositivo para la capacidad de eliminación de elementos.

Si el dispositivo admite la eliminación de elementos en su árbol [**IWiaItem2**](-wia-iwiaitem2.md) , llame al método **IWiaItem2::D eleteitem** para quitar el objeto **IWiaItem2** . Tenga en cuenta que este método solo elimina un objeto una vez que se han liberado todas las referencias al objeto. Si se produce un error en la eliminación de un elemento, \_ se devuelve E DELETEITEM. El valor numérico de este error aún no se ha definido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




