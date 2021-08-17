---
title: Objeto del lector sincrónico
description: Objeto del lector sincrónico
ms.assetid: 52a4891f-03bf-4d8a-ab7b-e9739db30bc3
keywords:
- Windows SDK de formato multimedia, objetos de lector sincrónicos
- Formato de sistemas avanzados (ASF), objetos de lector sincrónicos
- ASF (formato de sistemas avanzados), objetos de lector sincrónicos
- objects,synchronous reader objects
- lectores sincrónicos, objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 629f08684f996a611acaf00b913eaa8715869bdfd0219ea27994e2f8faf7c896
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197065"
---
# <a name="synchronous-reader-object"></a>Objeto del lector sincrónico

El objeto de lector sincrónico se usa para leer archivos multimedia digitales mediante llamadas sincrónicas.

La función [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)crea el objeto de lector sincrónico , que establece un puntero a una **interfaz IWMSyncReader.** Las demás interfaces admitidas por la interfaz de lector sincrónica se pueden obtener llamando al **método QueryInterface.**

El objeto de lector sincrónico admite las interfaces siguientes.



| Interfaz                                | Descripción                                                                                                                                                        |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)   | Establece y recupera información de encabezado, como [*metadatos, marcadores,*](wmformat-glossary.md)y así sucesivamente.                                            |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) | Enumera la información de códec disponible. Hereda todos los métodos de **IWMHeaderInfo**.                                                                      |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) | Admite tamaños de atributo grandes, nombres de atributo duplicados y compatibilidad con varios lenguajes. Hereda todos los métodos de **IWMHeaderInfo** **e IWMHeaderInfo2.** |
| [**IWMProfile**](iwmprofile.md)         | Proporciona acceso a la información de perfil del Windows multimedia cargado en el lector.                                                                       |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)       | Recupera el identificador único global (GUID), si lo hay, asociado al perfil. Hereda todos los métodos de **IWMProfile**.                               |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)       | Admite el uso compartido de ancho de banda y la información de priorización de flujos en el perfil. Hereda todos los métodos de **IWMProfile** **e IWMProfile2.**                |
| [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)   | Proporciona funcionalidades de lectura sincrónica para archivos multimedia digitales.                                                                                                 |
| [**IWMSyncReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2) | Proporciona compatibilidad para buscar códigos de tiempo de SMPTE y para asignar ejemplos manualmente. Hereda todos los métodos de **IWMSyncReader**.                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Objeto del lector**](reader-object.md)
</dt> <dt>

[**Lectura de archivos con el lector sincrónico**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




