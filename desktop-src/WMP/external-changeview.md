---
title: Método External.changeView
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método changeView cambia la vista en Reproductor de Windows Media.
ms.assetid: bd9d7d4b-ee4c-4d7c-92ef-dd0b8ab46d9d
keywords:
- método changeView Reproductor de Windows Media
- método changeView Reproductor de Windows Media , Clase externa
- Clase externa Reproductor de Windows Media , método changeView
topic_type:
- apiref
api_name:
- External.changeView
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa982e87e0a25fa8ae6cc80b428524844f60e2ec76f50d246e7b2a76b3ca942a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649375"
---
# <a name="externalchangeview-method"></a>Método External.changeView

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **método changeView** cambia la vista en Reproductor de Windows Media.

## <a name="syntax"></a>Sintaxis


```JScript
External.changeView(
  LibraryLocationType,
  LibraryLocationID,
  Filter,
  ViewParams
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LibraryLocationType* \[ En\]
</dt> <dd>

Constante [de ubicación de biblioteca](library-location-constants.md) que especifica el tipo de la nueva vista. Por ejemplo, la constante CPGenreID especifica que la nueva vista mostrará un género determinado.

</dd> <dt>

*LibraryLocationID* \[ En\]
</dt> <dd>

**Cadena** que contiene el identificador del elemento específico que se mostrará en la nueva vista. Por ejemplo, si *LibraryLocationType* es CPGenreID, este parámetro especifica el identificador del género que se va a mostrar en la nueva vista. Esta cadena puede estar vacía. Vea la sección Comentarios.

</dd> <dt>

*Filtro* \[ En\]
</dt> <dd>

**Cadena** que contiene el filtro de la nueva vista. La vista se filtrará como si el usuario hubiera escrito este texto en el control de rueda de palabras del reproductor. Esta cadena puede estar vacía.

</dd> <dt>

*ViewParams* \[ En\]
</dt> <dd>

**Cadena** que contiene parámetros que Reproductor de Windows Media pone a disposición de la nueva página de detección que se muestra con la nueva vista. Estos parámetros no se interpretan mediante Reproductor de Windows Media. Se crean mediante la tienda en línea y solo tienen significado para la tienda en línea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

En algunos casos, tiene sentido establecer el parámetro *LibraryLocationID* en la cadena vacía. Por ejemplo, si establece el parámetro *LibraryLocationType* en AllCPAlbumIDs, la nueva vista representará todos los álbumes. Ningún álbum individual será el foco de la nueva vista, por lo que no es necesario proporcionar un identificador de álbum en el *parámetro LibraryLocationID.*

El *parámetro ViewParams* proporciona una manera de que una página de detección se comunique con otra página de detección. Cuando el script de una página de detección llama **a changeView,** Reproductor de Windows Media ajusta su interfaz de usuario. Ese ajuste hace que el reproductor llame al método [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) del complemento para obtener la dirección URL de una nueva página de detección. La cadena que pasa la página de detección original en el *parámetro ViewParams* no se pasa a **GetTemplate.** Sin embargo, la nueva página de detección puede recuperar la cadena *ViewParams* llamando a [External.viewParameters.](external-viewparameters.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External.libraryLocationID**](external-librarylocationid.md)
</dt> <dt>

[**External.libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**External.viewParameters**](external-viewparameters.md)
</dt> </dl>

 

 





