---
title: Image Mastering API
description: Image Mastering API
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 641d9357496eb82a7e30f25a711928b16eeee2bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117583"
---
# <a name="image-mastering-api"></a>Image Mastering API

## <a name="purpose"></a>Propósito

La API de mastering de imágenes de Microsoft Windows permite a las aplicaciones almacenar y grabar imágenes en medios de almacenamiento óptico de CD, DVD y Dv-ray. Otros medios de tipo disco que menten imágenes de la misma manera también pueden usar esta API.

## <a name="developer-audience"></a>Audiencia de desarrolladores

IMAPI está diseñado para C/C++ y Visual Basic desarrolladores y aquellos que escriben scripts mediante VBScript.

Se recomienda conocer las tecnologías de CD, DVD y Dv-ray y los sistemas de archivos. Los desarrolladores pueden beneficiarse de la familiaridad con la revisión más reciente de Comando multimedia (MMC) [en ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go).

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

IMAPI 2.0 se admite de forma nativa a partir de Windows Vista y Windows Server 2008. La habilitación de la funcionalidad IMAPI 2.0 para Windows XP y Windows Server 2003 requiere la instalación del paquete de actualización [KB932716.](https://support.microsoft.com/kb/932716) Si este paquete no está instalado, Windows XP sigue siendo compatible de forma nativa con [IMAPI 1.0.](imapiv1.md)

> [!Note]  
> Windows Feature Pack para Storage está disponible para el público a través del Centro [de descarga de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05). Puede encontrar información adicional sobre los cambios específicos de la API en la sección [Novedades.](what-s-new.md)

 

## <a name="in-this-section"></a>En esta sección



| Tema                                             | Descripción                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [Novedades](what-s-new.md)<br/>           | Información que detalla cada versión significativa de Image Mastering API.<br/> |
| [Acerca de IMAPI](about-imapi.md)<br/>         | Información general sobre Image Mastering API.<br/>                         |
| [Uso de IMAPI](using-imapi.md)<br/>         | Temas relacionados con tareas que muestran cómo usar Image Mastering API.<br/>   |
| [Referencia de IMAPI](imapi-reference.md)<br/> | Descripciones detalladas de interfaces IMAPI y otros elementos de programación.<br/>  |



 

## <a name="additional-resources"></a>Recursos adicionales

Puede encontrar más información sobre IMAPI y otros temas relacionados en las siguientes ubicaciones:



|                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Microsoft Optical Storage Blog](/archive/blogs/opticalstorage/)                | Resalta los temas que se centran en la implementación de Image Mastering API en escenarios de desarrollo del mundo real.                                                                                                                                                                                                                                                 |
| [Foro de discusión de plataformas ópticas](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | Analice CDROM.SYS, IMAPIv2 y Live File System. Este foro se centra en temas de nivel de sistema y está destinado a desarrolladores de aplicaciones en lugar de usuarios finales.                                                                                                                                                                                                 |
| [T10 Technical Committee](https://www.t10.org/)                       | Un comité técnico del Comité Internacionales de Estándares de Tecnologías de la Información (INCITS) pronunciaba "conclusiones". INCITS está reconocido por y funciona según las reglas aprobadas por el American National Standards Institute (ANSI). Estas reglas están diseñadas para garantizar que los estándares voluntarias se desarrollan mediante el consenso de los grupos del sector. |
| [Asociación de tecnología de almacenamiento óptico ( TECHNOLOGY)](http://www.osta.org/) | Trabaja para dar forma al futuro del sector a través de reuniones periódicas de aplicaciones comerciales de almacenamiento óptico (COSA), compatibilidad de DVD, marketing, MPV (MusicPhotoVideo), comités de UDF y un nuevo comité de Blue. Las empresas interesadas de todo el mundo están invitadas a unirse a la organización y participar en sus comités y programas.               |



 

 

