---
description: La interfaz IWiaSegmentationFilter detecta subregiones de una secuencia de imágenes y crea elementos IWiaItem2 independientes para cada una de ellas.
ms.assetid: eb7f1284-ab98-4d86-8b30-7abd504cee12
title: Interfaz IWiaSegmentationFilter (WIA. h)
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
ms.openlocfilehash: b9c0bcdee5b40c37fb38b390f5085fe275f0f660
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908003"
---
# <a name="iwiasegmentationfilter-interface"></a>Interfaz IWiaSegmentationFilter

La interfaz **IWiaSegmentationFilter** detecta subregiones de una secuencia de imágenes y crea elementos [**IWiaItem2**](-wia-iwiaitem2.md) independientes para cada una de ellas.

## <a name="members"></a>Miembros

La interfaz **IWiaSegmentationFilter** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaSegmentationFilter** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWiaSegmentationFilter** tiene estos métodos.



| Método                                                             | Descripción                                                                                                                                              |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) | Determina las subregiones de una imagen que se distribuyen en la placa de plano, de modo que cada una de las subregiones pueda adquirirse en un elemento de imagen independiente. <br/> |



 

## <a name="remarks"></a>Observaciones

Una aplicación debe usar [**IWiaItem2:: getExtension**](-wia-iwiaitem2-getextension.md) para crear una nueva instancia del filtro de segmentación. Una aplicación normalmente llama a esta función antes de mostrar su ventana de vista previa.

Al implementar este filtro, use [**IWiaItem2:: CreateChildItem**](-wia-iwiaitem2-createchilditem.md) para crear los elementos secundarios. La aplicación debe pasar **\_ \_ \_ los valores de la propiedad primaria Copy** al parámetro *ICreationFlags* para asegurarse de que las propiedades, como el formato de imagen y la resolución, son las mismas en el elemento secundario recién creado como en el elemento primario.

Un filtro de segmentación debe admitir todos los formatos de imagen que admite el controlador con el que se usa. El filtro proporcionado por Microsoft admite mapas de bits (BMP), formato de intercambio de gráficos (GIF), JPEG, gráficos de red portátiles (PNG) y Tagged Image File Format (TIFF).

El filtro de segmentación solo se debe usar en elementos de película y escáner plano. En el análisis de películas, un escáner suele tener fotogramas fijos, en cuyo caso el controlador creó los elementos secundarios y la aplicación no debe invocar el filtro de segmentación.

La interfaz **IWiaSegmentationFilter** , al igual que todas las interfaces del modelo de objetos componentes (com), hereda los métodos de interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Métodos IUnknown                                        | Descripción                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Devuelve punteros a las interfaces compatibles. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa el recuento de referencias.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Reduce el recuento de referencias.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
