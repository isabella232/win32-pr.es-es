---
description: La interfaz IWiaSegmentationFilter detecta las subrecciones de un flujo de imagen y crea elementos IWiaItem2 independientes para cada una.
ms.assetid: eb7f1284-ab98-4d86-8b30-7abd504cee12
title: Interfaz IWiaSegmentationFilter (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 304b5be43aad8afc1730d2a23c170f11f11d319ffc4ae3eb13781efe09da2d41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659705"
---
# <a name="iwiasegmentationfilter-interface"></a>Interfaz IWiaSegmentationFilter

La **interfaz IWiaSegmentationFilter** detecta las subrecciones de un flujo de imagen y crea elementos [**IWiaItem2 independientes**](-wia-iwiaitem2.md) para cada una.

## <a name="members"></a>Miembros

La **interfaz IWiaSegmentationFilter** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaSegmentationFilter** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWiaSegmentationFilter** tiene estos métodos.



| Método                                                             | Descripción                                                                                                                                              |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) | Determina las subrecciones de una imagen colocadas en la placa plana para que cada una de las subrecciones se pueda adquirir en un elemento de imagen independiente. <br/> |



 

## <a name="remarks"></a>Comentarios

Una aplicación debe usar [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) para crear una nueva instancia del filtro de segmentación. Normalmente, una aplicación llama a esta función antes de mostrar su ventana de vista previa.

Al implementar este filtro, use [**IWiaItem2::CreateChildItem**](-wia-iwiaitem2-createchilditem.md) para crear los elementos secundarios. La aplicación debe pasar **COPY \_ PARENT PROPERTY \_ \_ VALUES** al parámetro *ICreationFlags* para asegurarse de que propiedades como el formato de imagen y la resolución son las mismas en el elemento secundario recién creado que en el elemento primario.

Un filtro de segmentación debe admitir todos los formatos de imagen que admite el controlador con el que se usa. El filtro proporcionado por Microsoft admite mapas de bits (BMP), Formato de intercambio de gráficos (GIF), JPEG, Portable Network Graphics (PNG) y Tagged Image File Format (TIFF).

El filtro de segmentación solo debe usarse en elementos de película y escáner plano. Para el examen de películas, un escáner suele incluir marcos fijos, en cuyo caso el controlador creó los elementos secundarios y la aplicación no debe invocar el filtro de segmentación.

La **interfaz IWiaSegmentationFilter,** al igual que todas las interfaces del modelo de objetos componentes (COM), hereda los métodos de interfaz [IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown)



| Métodos IUnknown                                        | Descripción                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Devuelve punteros a las interfaces compatibles. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa el recuento de referencias.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Reduce el recuento de referencias.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
