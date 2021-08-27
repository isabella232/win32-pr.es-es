---
title: Interfaces de persistencia
description: Interfaces de persistencia
ms.assetid: a93582b3-bdbf-430d-b4a6-c0df7bc35dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4894ccb1cc5d17747739e78918da9a5b48e2cca13a9f36078d752fceeaef011
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120425"
---
# <a name="persistence-interfaces"></a>Interfaces de persistencia

Los objetos que tienen un estado persistente de cualquier tipo deben implementar al menos una interfaz IPersist y, preferiblemente, varias interfaces, para proporcionar al contenedor la opción más flexible de cómo desea guardar el estado de un \* control.

Si un control tiene cualquier estado persistente, como mínimo, debe implementar [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) o [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) (los dos son mutuamente excluyentes y no deben implementarse juntos en su mayor parte). Este último se usa cuando un control desea saber cuándo se crea nuevo en lugar de volver a cargarse desde un estado persistente existente (**IPersistStream** no tiene la nueva funcionalidad creada). La existencia de cualquiera de las interfaces indica que el control puede guardar y cargar su estado persistente en una secuencia, es decir, una instancia de [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).

Más allá de estas dos interfaces basadas en secuencias, las interfaces IPersist enumeradas en la tabla siguiente se pueden proporcionar opcionalmente para admitir la persistencia en ubicaciones distintas de una \* [**IStream ampliable.**](/windows/desktop/api/objidl/nn-objidl-istream)

Se identifica un conjunto de categorías de componentes para cubrir la compatibilidad con interfaces de persistencia, vea [Categorías de componentes](component-categories.md).



| Interfaz                                                              | Uso                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))<br/>           | El objeto puede guardar y cargar su estado en una matriz de bytes secuenciales de longitud fija (en memoria).<br/>                                                                                                                                                                                                                                                    |
| [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/>                  | El objeto puede guardar y cargar su estado en una [**instancia de IStorage.**](/windows/desktop/api/objidl/nn-objidl-istorage) Los controles que deseen marcarse como Insertable como otros objetos de documento compuestos (para la inserción en contenedores que no tienen en cuenta el control) deben admitir esta interfaz.<br/>                                                                                               |
| [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)<br/> | El objeto puede guardar y cargar su estado como propiedades individuales escritas en IPropertyBag que implementa el contenedor. Esto se usa para la funcionalidad Guardar como texto en algunos contenedores.<br/>                                                                                                                                                          |
| [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/>  | El objeto puede guardar y cargar su estado en una ubicación denominada por un moniker. El control llama [**a IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) para recuperar la interfaz de almacenamiento que requiere, como [**IStorage,**](/windows/desktop/api/objidl/nn-objidl-istorage) [**IStream,**](/windows/desktop/api/objidl/nn-objidl-istream) [**ILockBytes,**](/windows/desktop/api/objidl/nn-objidl-ilockbytes) [**IDataObject,**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)etc.<br/> |



 

Aunque la compatibilidad [**con IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) es opcional, se recomienda encarecidamente como optimización para contenedores con características guardar como texto, como Visual Basic.

A excepción de [**IPersistStream::GetSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax), [**IPersistStreamInit::GetSizeMax**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-getsizemax)e [**IPersistMemory::GetSizeMax,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768208(v=vs.85))todos los métodos de cada interfaz deben estar totalmente implementados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles](controls.md)
</dt> </dl>

 

