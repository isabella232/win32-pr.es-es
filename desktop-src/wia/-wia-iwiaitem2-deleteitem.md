---
description: Quita el objeto IWiaItem2 actual del árbol de objetos del dispositivo.
ms.assetid: 247eb36f-3e5c-4030-8334-1a4028b3eb44
title: Método IWiaItem2::D eleteItem (Wia.h)
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
ms.openlocfilehash: 791d596ee48c4d3e2efd67259ec2e37249c930c6da32f704d332df1da6930503
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593005"
---
# <a name="iwiaitem2deleteitem-method"></a>IWiaItem2::D eleteItem (método)

Quita el objeto [**IWiaItem2**](-wia-iwiaitem2.md) actual del árbol de objetos del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeleteItem(
  [in] LONG lFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

Actualmente no se usa. Debe establecerse como cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

El sistema en tiempo de ejecución Windows Image Acquisition (WIA) 2.0 representa cada dispositivo de hardware WIA 2.0 conectado al equipo del usuario como un árbol jerárquico de objetos [**IWiaItem2.**](-wia-iwiaitem2.md) Un dispositivo WIA 2.0 determinado puede permitir o no que las aplicaciones eliminen objetos **IWiaItem2** de su árbol. Los elementos que tienen elementos secundarios no se pueden eliminar. La [**interfaz \_ \_ CAPS de IEnumWIA DEV**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) debe usarse para consultar la funcionalidad de eliminación de elementos en el dispositivo.

Si el dispositivo admite la eliminación de elementos en su árbol [**IWiaItem2,**](-wia-iwiaitem2.md) llame al método **IWiaItem2::D eleteItem** para quitar el objeto **IWiaItem2.** Tenga en cuenta que este método solo elimina un objeto después de que se hayan liberado todas las referencias al objeto. Si se ha dado un error en la eliminación de un elemento, se devuelve E \_ DELETEITEM. El valor numérico de este error aún no está definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




