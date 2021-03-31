---
title: API de procesamiento de imágenes
description: .
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc23c972cf111dee5edf3cb014a52351eda3605e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "103995708"
---
# <a name="image-mastering-api"></a>API de procesamiento de imágenes

## <a name="purpose"></a>Propósito

La API de Microsoft Windows Image Mastering permite a las aplicaciones almacenar en fases y grabar imágenes en medios de almacenamiento ópticos de CD, DVD y Blu-Ray. Otros medios similares a los discos que establecen imágenes de la misma manera también pueden usar esta API.

## <a name="developer-audience"></a>Audiencia de desarrolladores

IMAPi está diseñado para desarrolladores de C/C++ y Visual Basic y para los que escriben scripts con VBScript.

Se recomienda el conocimiento de las tecnologías y los sistemas de archivos de CD, DVD y Blu-Ray. Los desarrolladores pueden beneficiarse de una familiaridad con la última revisión del comando multimedia (MMC) en [FTP://ftp.T10.org/T10/drafts/MMC6](https://www.microsoft.com/?ref=go).

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

IMAPi 2,0 se admite de forma nativa a partir de Windows Vista y Windows Server 2008. La habilitación de la funcionalidad de IMAPi 2,0 para Windows XP y Windows Server 2003 requiere la instalación del paquete de actualización de [KB932716](https://support.microsoft.com/kb/932716) . Si este paquete no está instalado, Windows XP sigue siendo compatible de forma nativa con [imapi 1,0](imapiv1.md).

> [!Note]  
> Windows Feature Pack para el almacenamiento está disponible para el público a través del [centro de descarga de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05). Puede encontrar información adicional relacionada con los cambios específicos de la API en la sección [novedades](what-s-new.md) .

 

## <a name="in-this-section"></a>En esta sección



| Tema                                             | Descripción                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [Novedades](what-s-new.md)<br/>           | Información que detalla cada versión significativa de la API de masterización de imágenes.<br/> |
| [Acerca de IMAPi](about-imapi.md)<br/>         | Información general sobre la API de maestro de imágenes.<br/>                         |
| [Usar IMAPi](using-imapi.md)<br/>         | Temas relacionados con tareas que muestran cómo usar la API de maestro de imágenes.<br/>   |
| [Referencia de IMAPi](imapi-reference.md)<br/> | Descripciones detalladas de las interfaces de IMAPi y otros elementos de programación.<br/>  |



 

## <a name="additional-resources"></a>Recursos adicionales

Puede encontrar más información sobre IMAPi y otros temas relacionados en las siguientes ubicaciones:



|                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Blog de Microsoft Optical Storage](/archive/blogs/opticalstorage/)                | Destaca los temas que se centran en la implementación de la API de creación de imágenes maestras en escenarios de desarrollo reales.                                                                                                                                                                                                                                                 |
| [Foro de discusión de plataforma óptica](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | Comente los problemas de CDROM.SYS, IMAPIv2 y del sistema de archivos LFS. Este foro se centra en los temas de nivel de sistema y está destinado a los desarrolladores de aplicaciones en lugar de a endusers.                                                                                                                                                                                                 |
| [Comité técnico de T10](https://www.t10.org/)                       | Un Comité técnico del Comité Internacional sobre estándares de tecnología de la información (INCITS, pronunciado "información"). INCITS es acreditado por y funciona en reglas aprobadas por el American National Standards Institute (ANSI). Estas reglas están diseñadas para garantizar que los estándares voluntarios se desarrollan por el consenso de los grupos del sector. |
| [Asociación de tecnología de almacenamiento óptico (OSTA)](http://www.osta.org/) | Trabaja para dar forma al futuro del sector a través de reuniones periódicas de aplicaciones de almacenamiento óptico comercial (COSA), compatibilidad con DVD, marketing, MPV (MusicPhotoVideo), comités de UDF y un nuevo Comité de láser Blue ad hoc. Las compañías interesadas en todo el mundo están invitadas a unirse a la organización y participar en sus comités y programas.               |



 

 

