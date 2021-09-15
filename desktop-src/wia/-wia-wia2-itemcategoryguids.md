---
description: Windows Los elementos de Adquisición de imágenes (WIA) 2.0 se agrupan en categorías que definen cómo se va a tratar o usar un IWiaItem2.
ms.assetid: 927f4957-aedf-4eef-8892-91cf9b56e1a2
title: GUID de la categoría de elementos de WIA 2.0 (Wiadef.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574389"
---
# <a name="wia-20-item-category-guids"></a>GUID de la categoría de elementos de WIA 2.0

Windows Los elementos de Adquisición de imágenes (WIA) 2.0 se agrupan en categorías que definen cómo se va a tratar o usar [**un IWiaItem2.**](-wia-iwiaitem2.md) Por ejemplo, si el elemento representa un feeder, la aplicación debe esperar que contenga las propiedades de fuente de documentos necesarias y funcione como un feeder de documentos. Si el elemento representa un archivo terminado, una aplicación WIA 2.0 debe tratarlo de este modo, suponiendo que los datos son estáticos y se encuentran en el dispositivo. (Las reglas de cada elemento se definirán en sus documentos de especificación individuales). Cada categoría tiene una constante de tipo GUID.



| Constante                                                                                                                                                                                               | Descripción                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_CATEGORY_AUTO"></span><span id="wia_category_auto"></span><dl> <dt>**WIA \_ CATEGORY \_ AUTO**</dt> </dl>                             | Elemento que representa los valores de configuración automática para un dispositivo de escáner WIA 2.0 que admite el examen configurado automáticamente.<br/>                                   |
| <span id="WIA_CATEGORY_FEEDER"></span><span id="wia_category_feeder"></span><dl> <dt>**FUENTE DE \_ CATEGORÍA DE WIA \_**</dt> </dl>                       | Elemento de fuente que es un origen de datos programable y sigue las reglas estándar y los conjuntos de propiedades necesarios para admitir los fuentes de documentos.<br/>                             |
| <span id="WIA_CATEGORY_FEEDER_BACK"></span><span id="wia_category_feeder_back"></span><dl> <dt>**FUENTE DE \_ DISTRIBUCIÓN DE \_ CATEGORÍA WIA DE \_ NUEVO**</dt> </dl>       | Origen de datos programable que describe el origen de datos del lado posterior de un elemento de fuente base dúplex.<br/>                                                                       |
| <span id="WIA_CATEGORY_FEEDER_FRONT"></span><span id="wia_category_feeder_front"></span><dl> <dt>**WIA \_ CATEGORY \_ FEEDER \_ FRONT**</dt> </dl>    | Origen de datos programable que describe el origen de datos del lado frontal de un elemento de fuente base dúplex.<br/>                                                                      |
| <span id="WIA_CATEGORY_FILM"></span><span id="wia_category_film"></span><dl> <dt>**WIA \_ CATEGORY \_ PELÍCULAS**</dt> </dl>                             | Elemento de película que es un origen de datos programable y sigue las reglas estándar y los conjuntos de propiedades necesarios para admitir unidades de análisis de películas.<br/>                            |
| <span id="WIA_CATEGORY_FINISHED_FILE"></span><span id="wia_category_finished_file"></span><dl> <dt>**ARCHIVO FINALIZADO \_ DE LA \_ CATEGORÍA \_ WIA**</dt> </dl> | Elemento que no es un origen de datos programable, un elemento que proporciona datos en un formato de archivo finalizado o un elemento de carpeta que contiene elementos de formato de archivo finalizados.<br/> |
| <span id="WIA_CATEGORY_FLATBED"></span><span id="wia_category_flatbed"></span><dl> <dt>**WIA \_ CATEGORY \_ FLATBED**</dt> </dl>                    | Elemento plano que es un origen de datos programable y sigue las reglas estándar y los conjuntos de propiedades necesarios para admitir el examen de la placa plana.<br/>                     |
| <span id="WIA_CATEGORY_FOLDER"></span><span id="wia_category_folder"></span><dl> <dt>**CARPETA DE \_ CATEGORÍA DE \_ WIA**</dt> </dl>                       | Un elemento de almacenamiento de carpetas (no un origen de datos programable) que contiene otros elementos de carpeta o archivos terminados o ambos.<br/>                                                     |
| <span id="WIA_CATEGORY_ROOT"></span><span id="wia_category_root"></span><dl> <dt>**RAÍZ DE CATEGORÍA DE WIA \_ \_**</dt> </dl>                             | Elemento raíz del dispositivo. <br/>                                                                                                                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 




