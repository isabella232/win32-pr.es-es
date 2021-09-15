---
title: Objeto del lector
description: Objeto del lector
ms.assetid: b5edbf8b-820f-4e09-a482-8efc2283360e
keywords:
- Windows SDK de formato multimedia, objetos de lector
- Formato de sistemas avanzados (ASF), objetos de lector
- ASF (formato de sistemas avanzados), objetos de lector
- objects,reader objects
- objetos de lector, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7958689fa7744286c92c294219fb2c963e55c860
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466680"
---
# <a name="reader-object"></a>Objeto del lector

El objeto lector lee ejemplos de datos de archivos multimedia. Actualmente, el objeto reader admite archivos que usan la estructura de archivos de formato de sistemas avanzados (ASF), así como archivos MP3. Los datos entregados por el objeto lector están descomprimidos y listos para su representación de forma predeterminada, aunque los ejemplos se pueden entregar sin descomprimir si lo desea. Los ejemplos se entregan de forma asincrónica desde el objeto de lector; debe configurar una función de devolución de llamada para recibirlas. Para la reproducción sincrónica de archivos ASF, use el objeto de lector sincrónico. Ni el lector ni el lector sincrónico representan ningún dato. Debe proporcionar sus propias rutinas de representación para mostrar los medios recuperados de un archivo.

Cuando un archivo contiene medios codificados que se pueden descodificar con un códec compatible con el objeto lector, puede controlar el formato de la salida sin comprimir. Para cambiar el formato de salida descomprimida de una secuencia, debe recuperar el objeto de propiedades de medios de salida predeterminado para esa secuencia, realizar cambios en él y reasignarlo a la secuencia en el lector. Los objetos de propiedades de medios de salida están subordinados al objeto de lector y solo se deben crear mediante el [**método IWMReader::GetOutputProps.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops)

La función [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)crea el objeto lector , que establece un puntero a una **interfaz IWMReader.** Las demás interfaces del objeto de lector se pueden obtener llamando al **método QueryInterface.**

El objeto lector admite las interfaces siguientes.



| Interfaz                                                    | Descripción                                                                                                                                                                     |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IReferenceClock**](ireferenceclock.md)                   | Proporciona acceso al reloj del sistema utilizado por el lector.                                                                                                                         |
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)                         | Administra la adquisición de licencias, [*las propiedades drm*](wmformat-glossary.md) y la individualización de cliente.                                  |
| [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)                       | Proporciona acceso a las licencias que usan niveles de protección de salida (OPL) para especificar derechos.                                                                                          |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)                       | Establece y recupera información de encabezado, [*incluidos metadatos, marcadores*](wmformat-glossary.md)y datos de script.                                                 |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)                     | Recupera información sobre los códecs que se usaron para codificar el contenido del archivo. Hereda todos los métodos de **IWMHeaderInfo**.                                      |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)                     | Admite tamaños de atributo grandes, nombres de atributo duplicados y compatibilidad con varios idiomas. Hereda todos los métodos de **IWMHeaderInfo** **e IWMHeaderInfo2.**              |
| [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)                       | Recupera el tamaño del paquete más grande del archivo cargado en el lector.                                                                                                      |
| [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)                     | Recupera el tamaño del paquete más pequeño del archivo cargado en el lector.                                                                                                     |
| [**IWMProfile**](iwmprofile.md)                             | Proporciona acceso a la información de perfil del archivo cargado en el lector.                                                                                                    |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)                           | Recupera el identificador único global (GUID), si lo hay, asociado al perfil. Hereda todos los métodos de **IWMProfile**.                                            |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)                           | Admite el uso compartido de ancho de banda y la información de priorización de flujos en el perfil. Hereda todos los métodos de **IWMProfile** **e IWMProfile2.**                             |
| [**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)                               | Proporciona funcionalidades básicas de lectura de archivos, incluidas operaciones como abrir, cerrar, iniciar, pausar, reanudar, detener y obtener y establecer las propiedades de salida.                  |
| [**IWMReaderAccelerator**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator)         | Se comunica con la aceleración de vídeo de DirectX.                                                                                                                                   |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)               | Proporciona características avanzadas del lector, como un reloj proporcionado por el usuario, asignación de búfer, estadísticas de devolución y notificaciones de selección de secuencias.                              |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)             | Proporciona un intervalo adicional de métodos avanzados para un objeto de lector existente. Hereda todos los métodos de **IWMReaderAdvanced.**                                           |
| [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)             | Proporciona búsqueda avanzada y control de streaming. Hereda todos los métodos de **IWMReaderAdvanced** **e IWMReaderAdvanced2**.                                               |
| [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)             | Proporciona opciones avanzadas de lector, incluida la compatibilidad con varios idiomas. Hereda todos los métodos de **IWMReaderAdvanced,** **IWMReaderAdvanced2** e **IWMReaderAdvanced3**. |
| [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)     | Controla las opciones de configuración de red.                                                                                                                                        |
| [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2)   | Proporciona acceso a opciones avanzadas de configuración de red. Hereda todos los métodos de **IWMReaderNetworkConfig**.                                                          |
| [**IWMReaderStreamClock**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderstreamclock)         | Establece y cancela temporizadores en los relojes de secuencia y recupera el valor actual de un reloj de secuencia especificado.                                                                          |
| [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode)               | Proporciona información sobre los intervalos de código de tiempo de SMPTE en el archivo cargado en el lector.                                                                                             |
| [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation) | Comprueba si los cambios en las propiedades de salida de una secuencia funcionan correctamente.                                                                                                |



 

Las siguientes interfaces de devolución de llamada se pueden implementar en la aplicación para realizar un seguimiento del progreso de un objeto de lector.



| Interfaz                                                      | Descripción                                                                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)         | Adquiere las credenciales de los usuarios y comprueba que tienen permiso para acceder a un sitio remoto.                                               |
| [**IWMReaderAllocatorEx**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderallocatorex)           | Proporciona alternativas expandidas a los **métodos AllocateForOutput** y **AllocateForStream** de la **interfaz IWMReaderCallbackAdvanced.** |
| [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)                 | Proporciona métodos de devolución de llamada **para los métodos Start** y **Open** **de IWMReader**.                                                            |
| [**IWMReaderCallbackAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced) | Proporciona métodos de devolución de llamada para los métodos de [**la interfaz IWMReaderAdvanced.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)                                    |
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)                 | Se requiere cuando se debe comunicar la información de estado a la aplicación host.                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Lectura de archivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Objeto del lector sincrónico**](synchronous-reader-object.md)
</dt> </dl>

 

 




