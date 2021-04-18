---
description: Los elementos de adquisición de imágenes de Windows (WIA) 2,0 se agrupan en categorías que definen cómo se trata o se usa un IWiaItem2.
ms.assetid: 927f4957-aedf-4eef-8892-91cf9b56e1a2
title: GUID de categoría de elemento de WIA 2,0 (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CATEGORY_AUTO
- WIA_CATEGORY_FEEDER
- WIA_CATEGORY_FEEDER_BACK
- WIA_CATEGORY_FEEDER_FRONT
- WIA_CATEGORY_FILM
- WIA_CATEGORY_FINISHED_FILE
- WIA_CATEGORY_FLATBED
- WIA_CATEGORY_FOLDER
- WIA_CATEGORY_ROOT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: e2785d7d82e28641ebeefad730f02b3561a537a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715170"
---
# <a name="wia-20-item-category-guids"></a>GUID de categoría de elemento de WIA 2,0

Los elementos de adquisición de imágenes de Windows (WIA) 2,0 se agrupan en categorías que definen cómo se trata o se usa un [**IWiaItem2**](-wia-iwiaitem2.md) . Por ejemplo, si el elemento representa un alimentador, la aplicación debe esperar que contenga las propiedades necesarias del alimentador de documentos y que funcione como un alimentador de documentos. Si el elemento representa un archivo terminado, una aplicación WIA 2,0 debe tratarlo de este modo, suponiendo que los datos son estáticos y se encuentran en el dispositivo. (Las reglas de cada elemento se definirán en sus documentos de especificación individuales). Cada categoría tiene una constante de tipo GUID.



| Constante                                                                                                                                                                                               | Descripción                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_CATEGORY_AUTO"></span><span id="wia_category_auto"></span><dl> <dt>**Categoría de WIA \_ \_ auto**</dt> </dl>                             | Un elemento que representa la configuración automática para un dispositivo de escáner WIA 2,0 que admite el análisis configurado automáticamente.<br/>                                   |
| <span id="WIA_CATEGORY_FEEDER"></span><span id="wia_category_feeder"></span><dl> <dt>**\_alimentador de categoría WIA \_**</dt> </dl>                       | Un elemento del alimentador que es un origen de datos programable y sigue las reglas estándar y los conjuntos de propiedades necesarios para admitir los alimentadores de documentos.<br/>                             |
| <span id="WIA_CATEGORY_FEEDER_BACK"></span><span id="wia_category_feeder_back"></span><dl> <dt>**\_alimentador de categoría WIA \_ \_ atrás**</dt> </dl>       | Origen de datos programable que describe el origen de datos de la parte posterior de un elemento de alimentador de base dúplex.<br/>                                                                       |
| <span id="WIA_CATEGORY_FEEDER_FRONT"></span><span id="wia_category_feeder_front"></span><dl> <dt>**\_alimentador de categoría WIA \_ \_ delantero**</dt> </dl>    | Origen de datos programable que describe el origen de datos de front-end de un elemento de alimentador de base dúplex.<br/>                                                                      |
| <span id="WIA_CATEGORY_FILM"></span><span id="wia_category_film"></span><dl> <dt>**\_película de categoría WIA \_**</dt> </dl>                             | Un elemento de película que es un origen de datos programable y sigue las reglas estándar y los conjuntos de propiedades necesarios para admitir las unidades de análisis de películas.<br/>                            |
| <span id="WIA_CATEGORY_FINISHED_FILE"></span><span id="wia_category_finished_file"></span><dl> <dt>**archivo de categoría de WIA \_ \_ finalizada \_**</dt> </dl> | Un elemento que no es un origen de datos programable, o un elemento que proporciona los datos en un formato de archivo terminado, o un elemento de carpeta que contiene los elementos de formato de archivo finalizados.<br/> |
| <span id="WIA_CATEGORY_FLATBED"></span><span id="wia_category_flatbed"></span><dl> <dt>**plano de la \_ categoría WIA \_**</dt> </dl>                    | Un elemento plano que es un origen de datos programable y sigue las reglas estándar y los conjuntos de propiedades necesarios para admitir el análisis de placas de plano.<br/>                     |
| <span id="WIA_CATEGORY_FOLDER"></span><span id="wia_category_folder"></span><dl> <dt>**\_carpeta de categoría WIA \_**</dt> </dl>                       | Elemento de almacenamiento en carpetas (no es un origen de datos programable) que contiene otros elementos de carpeta o archivos finalizados o ambos.<br/>                                                     |
| <span id="WIA_CATEGORY_ROOT"></span><span id="wia_category_root"></span><dl> <dt>**raíz de la \_ categoría WIA \_**</dt> </dl>                             | Elemento raíz para el dispositivo. <br/>                                                                                                                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




