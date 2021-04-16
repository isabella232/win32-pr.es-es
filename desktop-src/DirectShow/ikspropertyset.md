---
description: 'La interfaz IKsPropertySet se diseñó originalmente como una forma eficaz de establecer y recuperar las propiedades del dispositivo en los controladores WDM, mediante KSProxy para traducir las llamadas a métodos COM en modo de usuario en los conjuntos de propiedades de modo kernel utilizados por los controladores de clase de transmisión por secuencias WDM. Esta interfaz se usa ahora también para pasar información de forma estricta entre los componentes de software. En algunos casos, los componentes de software deben implementar esta interfaz, o bien la interfaz IKsControl (documentada en el DDK de DirectShow). Por ejemplo, si está escribiendo un descodificador MPEG-2 de software para usarlo con el navegador de DVD, debe implementar una de estas interfaces y también admitir los conjuntos de propiedades relacionados con el DVD que el navegador enviará al descodificador. Los pin pueden admitir una de estas interfaces para permitir que otros PIN o filtros establezcan o recuperen sus propiedades. Nota: existe otra interfaz con este nombre en el archivo de encabezado dsound. h. Las dos interfaces no son compatibles. La interfaz IKsControl, documentada en el DDK de DirectShow, es ahora la interfaz recomendada para pasar conjuntos de propiedades entre controladores WDM y componentes de modo de usuario. .'
ms.assetid: df26341d-f2d5-4a4e-954e-705e07415808
title: Interfaz IKsPropertySet (ksproxy. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 49a1f897d79a7514600f0c6553f931411aae8993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494332"
---
# <a name="ikspropertyset-interface"></a>Interfaz IKsPropertySet

La `IKsPropertySet` interfaz se diseñó originalmente como una forma eficaz de establecer y recuperar las propiedades del dispositivo en los controladores WDM, mediante KSProxy para traducir las llamadas a métodos com en modo de usuario en los conjuntos de propiedades de modo kernel usados por los controladores de clase de transmisión por secuencias WDM. Esta interfaz se usa ahora también para pasar información de forma estricta entre los componentes de software.

En algunos casos, los componentes de software deben implementar esta interfaz, o bien la interfaz **IKsControl** (documentada en el DDK de DirectShow). Por ejemplo, si está escribiendo un descodificador MPEG-2 de software para usarlo con el [navegador de DVD](dvd-navigator-filter.md), debe implementar una de estas interfaces y también admitir los conjuntos de propiedades relacionados con el DVD que el navegador enviará al descodificador. Los pin pueden admitir una de estas interfaces para permitir que otros PIN o filtros establezcan o recuperen sus propiedades.

> [!Note]  
> Existe otra interfaz con este nombre en el archivo de encabezado dsound. h. Las dos interfaces no son compatibles. La interfaz **IKsControl** , documentada en el DDK de DirectShow, es ahora la interfaz recomendada para pasar conjuntos de propiedades entre controladores WDM y componentes de modo de usuario.

 

## <a name="members"></a>Miembros

La interfaz **IKsPropertySet** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IKsPropertySet** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IKsPropertySet** tiene estos métodos.



| Método                                                  | Descripción                                                                          |
|:--------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**Obtener**](ikspropertyset-get.md)                       | Recupera una propiedad identificada por un GUID de conjunto de propiedades y un identificador de propiedad.<br/> |
| [**QuerySupported**](ikspropertyset-querysupported.md) | Determina si un objeto admite un conjunto de propiedades especificado.<br/>           |
| [**Conjunto**](ikspropertyset-set.md)                       | Establece una propiedad identificada por un GUID de conjunto de propiedades y un identificador de propiedad.<br/>      |



 

## <a name="remarks"></a>Observaciones

Debe incluir KS. h antes de ksproxy. h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Ksproxy. h</dt> </dl>    |
| Biblioteca<br/>                  | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 
