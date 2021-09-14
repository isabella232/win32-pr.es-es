---
description: La interfaz IKsPropertySet se diseñó originalmente como una manera eficaz de establecer y recuperar propiedades de dispositivo en controladores WDM, mediante KSProxy para traducir las llamadas al método COM en modo de usuario en los conjuntos de propiedades en modo kernel usados por los controladores de clases de streaming de WDM. Esta interfaz también se usa ahora para pasar información estrictamente entre los componentes de software. En algunos casos, los componentes de software deben implementar esta interfaz o, de lo contrario, la interfaz IKsControl (documentada en DirectShow DDK). Por ejemplo, si está escribiendo un descodificador MPEG-2 de software para su uso con el navegador de DVD, debe implementar una de estas interfaces y también admitir los conjuntos de propiedades relacionados con DVD que el navegador enviará al descodificador. Los pines pueden admitir una de estas interfaces para permitir que otros pines o filtros establezcan o recuperen sus propiedades. Nota Existe otra interfaz por este nombre en el archivo de encabezado d sound.h. Las dos interfaces no son compatibles. La interfaz IKsControl, documentada en el DDK de DirectShow, es ahora la interfaz recomendada para pasar conjuntos de propiedades entre los controladores WDM y los componentes del modo de usuario. .
ms.assetid: df26341d-f2d5-4a4e-954e-705e07415808
title: Interfaz IKsPropertySet (Ksproxy.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127275164"
---
# <a name="ikspropertyset-interface"></a>Interfaz IKsPropertySet

La interfaz se diseñó originalmente como una manera eficaz de establecer y recuperar propiedades de dispositivo en controladores WDM, mediante KSProxy para traducir las llamadas al método COM en modo de usuario en los conjuntos de propiedades de modo kernel usados por los controladores de clase de streaming de `IKsPropertySet` WDM. Esta interfaz también se usa ahora para pasar información estrictamente entre los componentes de software.

En algunos casos, los componentes de software deben implementar esta interfaz o, de lo contrario, la interfaz **IKsControl** (documentada en DirectShow DDK). Por ejemplo, si está escribiendo un descodificador MPEG-2 de software para su uso con el navegador [de DVD,](dvd-navigator-filter.md)debe implementar una de estas interfaces y también admitir los conjuntos de propiedades relacionados con DVD que el navegador enviará al descodificador. Los pines pueden admitir una de estas interfaces para permitir que otros pines o filtros establezcan o recuperen sus propiedades.

> [!Note]  
> Existe otra interfaz por este nombre en el archivo de encabezado d sound.h. Las dos interfaces no son compatibles. La **interfaz IKsControl,** documentada en el DDK de DirectShow, es ahora la interfaz recomendada para pasar conjuntos de propiedades entre los controladores WDM y los componentes del modo de usuario.

 

## <a name="members"></a>Members

La **interfaz IKsPropertySet** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IKsPropertySet también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IKsPropertySet** tiene estos métodos.



| Método                                                  | Descripción                                                                          |
|:--------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**Obtener**](ikspropertyset-get.md)                       | Recupera una propiedad identificada por un GUID del conjunto de propiedades y un identificador de propiedad.<br/> |
| [**QuerySupported**](ikspropertyset-querysupported.md) | Determina si un objeto admite un conjunto de propiedades especificado.<br/>           |
| [**Set**](ikspropertyset-set.md)                       | Establece una propiedad identificada por un GUID del conjunto de propiedades y un identificador de propiedad.<br/>      |



 

## <a name="remarks"></a>Observaciones

Debe incluir Ks.h antes que Ksproxy.h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Ksproxy.h</dt> </dl>    |
| Biblioteca<br/>                  | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 
