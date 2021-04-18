---
title: Objeto del lector sincrónico
description: Objeto del lector sincrónico
ms.assetid: 52a4891f-03bf-4d8a-ab7b-e9739db30bc3
keywords:
- SDK de Windows Media Format, objetos de lector sincrónicos
- Advanced Systems Format (ASF), objetos de lector sincrónicos
- ASF (formato de sistemas avanzados), objetos de lector sincrónicos
- objetos, objetos de lectura sincrónicos
- lectores sincrónicos, objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491fed915a049dbfc52acc24d06a0344d8e3109c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "105704918"
---
# <a name="synchronous-reader-object"></a>Objeto del lector sincrónico

El objeto lector sincrónico se utiliza para leer archivos multimedia digitales mediante llamadas sincrónicas.

La función [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)crea el objeto de lector sincrónico, que establece un puntero a una interfaz **IWMSyncReader** . Las otras interfaces que admite la interfaz de lectura sincrónica se pueden obtener llamando al método **QueryInterface** .

El objeto lector sincrónico admite las siguientes interfaces.



| Interfaz                                | Descripción                                                                                                                                                        |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)   | Establece y recupera información de encabezado, como metadatos, [*marcadores*](wmformat-glossary.md), etc.                                            |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) | Enumera la información de códec disponible. Hereda todos los métodos de **IWMHeaderInfo**.                                                                      |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) | Admite tamaños de atributo grandes, nombres de atributos duplicados y compatibilidad con varios idiomas. Hereda todos los métodos de **IWMHeaderInfo** y **IWMHeaderInfo2**. |
| [**IWMProfile**](iwmprofile.md)         | Proporciona acceso a la información de perfil del archivo de Windows Media cargado en el lector.                                                                       |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)       | Recupera el identificador único global (GUID), si existe, asociado al perfil. Hereda todos los métodos de **IWMProfile**.                               |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)       | Admite el uso compartido de ancho de banda y la información de priorización de flujo en el perfil. Hereda todos los métodos de **IWMProfile** y **IWMProfile2**.                |
| [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)   | Proporciona capacidades de lectura sincrónica para archivos multimedia digitales.                                                                                                 |
| [**IWMSyncReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2) | Proporciona compatibilidad para buscar códigos de tiempo SMPTE y para asignar ejemplos manualmente. Hereda todos los métodos de **IWMSyncReader**.                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**de la empresa**](objects.md)
</dt> <dt>

[**Objeto del lector**](reader-object.md)
</dt> <dt>

[**Leer archivos con el lector sincrónico**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




