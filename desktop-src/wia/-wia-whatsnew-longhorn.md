---
description: Muchas de las Windows API de adquisición de imágenes (WIA) se incluyen en Windows Image Acquisition (WIA) 2.0.
ms.assetid: d8e85c34-d8ce-4512-af71-102a21393fdf
title: Novedades de Windows image acquisition (WIA) 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fef5fdc2f70c7b0a7c25e3e9df68b82d05b7fd1a53eb7ec3613962f975e5c1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592955"
---
# <a name="whats-new-in-windows-image-acquisition-wia-20"></a>Novedades de Windows image acquisition (WIA) 2.0

Muchas de las Windows API de adquisición de imágenes (WIA) se incluyen en Windows Image Acquisition (WIA) 2.0. Además, hay algunas incompatibilidades hacia delante y hacia atrás entre Windows Image Acquisition (WIA) 1.0 y el servicio WIA 2.0 que se suministra con Windows Vista. Algunas interfaces, estructuras, propiedades y valores de propiedad de WIA 1.0 no son compatibles con y las aplicaciones que las usan no se ejecutarán en, Windows Vista y versiones posteriores. De forma similar, las aplicaciones que usan las nuevas interfaces, estructuras, propiedades y valores de propiedad introducidos con WIA 2.0 (consulte a continuación) no se ejecutarán en versiones del sistema operativo anteriores a Windows Vista.

## <a name="new-api-for-wia-20"></a>Nueva API para WIA 2.0

### <a name="constants-lists-updated-for-wia-20"></a>Constantes: listas actualizadas para WIA 2.0

-   [**Constantes comunes de propiedad de elemento de WIA**](-wia-wiaitempropcommonitem.md)
-   [**Constantes de propiedades de información de dispositivo**](-wia-wiadeviceinfoprop.md)
-   [**Constantes de propiedad del dispositivo del analizador**](-wia-wiaitempropscannerdevice.md)
-   [**Constantes de propiedad de elemento WIA del analizador**](-wia-wiaitempropscanneritem.md)
-   [**GUID de la categoría de elementos de WIA 2.0**](-wia-wia2-itemcategoryguids.md)
-   [**Constantes de tamaño de página de WIA 2.0**](-wia-wia2-pagesizeconstants.md)
-   [**Marcas de tipo de elemento WIA**](-wia-wia-item-type-flags.md)

### <a name="new-structures-in-wia-20"></a>Nuevas estructuras en WIA 2.0



| Tema                                               | Contenido                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) | Define los datos necesarios para llamar a un cuadro de diálogo de dispositivo.<br/>                                                                                                                                                                                                       |
| [**ENCABEZADO SIN PROCESAR DE WIA \_ \_**](-wia-wia-raw-header.md)     | La [**estructura WIA \_ RAW \_ HEADER**](-wia-wia-raw-header.md) define una imagen en el formato de datos RAW de un dispositivo y permite a las aplicaciones usar el formato RAW en las transferencias WIA.<br/>                                                                         |
| [**WiaTransferParams**](-wia-wiatransferparams.md) | [**WiaTransferParams**](-wia-wiatransferparams.md) se transmite a una aplicación durante una transferencia de datos por el sistema en tiempo de ejecución de WIA al [**método IWiaTransferCallback::TransferCallback.**](-wia-iwiatransfercallback-transfercallback.md)<br/> |



 

### <a name="new-interfaces-in-wia-20"></a>Nuevas interfaces en WIA 2.0



| Tema                                                         | Contenido                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)                   | Lo usan las aplicaciones para enumerar [**objetos IWiaItem2**](-wia-iwiaitem2.md) en la carpeta actual del árbol de elementos.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**IScanProfile**](-wia-iscanprofile.md)                     | La [**interfaz IScanProfile**](-wia-iscanprofile.md) representa un único perfil de examen y permite a las aplicaciones establecer y obtener las propiedades del perfil. <br/>                                                                                                                                                                                                                                                                                                                                   |
| [**IScanProfileMgr**](-wia-iscanprofilemgr.md)               | La [**interfaz IScanProfileMgr**](-wia-iscanprofilemgr.md) proporciona métodos para crear, abrir, eliminar y administrar perfiles de examen. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**IScanProfileUI**](-wia-iscanprofileui.md)                 | La [**interfaz IScanProfileUI permite**](-wia-iscanprofileui.md) a las aplicaciones mostrar un cuadro de diálogo para que los usuarios puedan crear, modificar y eliminar perfiles de examen.<br/>                                                                                                                                                                                                                                                                                                                               |
| [**IWiaAppErrorHandler**](-wia-iwiaapperrorhandler.md)       | La [**interfaz IWiaAppErrorHandler**](-wia-iwiaapperrorhandler.md) permite a las aplicaciones mostrar ventanas de error (durante las transferencias de datos) desde las que el usuario puede elegir si desea continuar, cancelar o anular la transferencia.<br/>                                                                                                                                                                                                                                                                     |
| [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)                       | La [**interfaz IWiaDevMgr2**](-wia-iwiadevmgr2.md) se usa para crear y administrar dispositivos de adquisición de imágenes y para registrarse para recibir eventos de dispositivo.<br/>                                                                                                                                                                                                                                                                                                                                             |
| [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md)             | La [**interfaz IWiaErrorHandler**](-wia-iwiaerrorhandler.md) proporciona métodos para controlar los errores que pueden producirse cuando una aplicación solicita datos de imagen, ya sea para la versión preliminar o los bits finales. <br/>                                                                                                                                                                                                                                                                                                      |
| [**IWiaImageFilter**](-wia-iwiaimagefilter.md)               | La [**interfaz IWiaImageFilter es**](-wia-iwiaimagefilter.md) una interfaz de extensión implementada por los desarrolladores de filtros de procesamiento de imágenes y a la que llama WIA 2.0. <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**IWiaItem2**](-wia-iwiaitem2.md)                           | La [**interfaz IWiaItem2**](-wia-iwiaitem2.md) proporciona a las aplicaciones la misma funcionalidad que la interfaz [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (la capacidad de consultar dispositivos para detectar sus funcionalidades, acceder a interfaces de transferencia de datos y propiedades de elementos y controlar el dispositivo). También proporciona a la aplicación la capacidad de crear y usar dinámicamente filtros de procesamiento de imágenes que pueden ser extensiones de los controladores de dispositivo WIA 2.0 proporcionados en Windows Vista.<br/> |
| [**IWiaPreview**](-wia-iwiapreview.md)                       | La [**interfaz IWiaPreview**](-wia-iwiapreview.md) almacena en caché imágenes sin filtrar internamente y las pasa a través de filtros de procesamiento de imágenes. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md) | La [**interfaz IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md) detecta las subrecciones de un flujo de imagen y crea elementos [**IWiaItem2**](-wia-iwiaitem2.md) independientes para cada una. <br/>                                                                                                                                                                                                                                                                                                         |
| [**IWiaTransfer**](-wia-iwiatransfer.md)                     | La [**interfaz IWiaTransfer**](-wia-iwiatransfer.md) proporciona transferencia de datos basada en secuencias. <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**IWiaTransferCallback**](-wia-iwiatransfercallback.md)     | La [**interfaz IWiaTransferCallback recibe**](-wia-iwiatransfercallback.md) devoluciones de llamada durante una transferencia de datos. <br/>                                                                                                                                                                                                                                                                                                                                                                                |
| [**IWiaUIExtension2**](-wia-iwiauiextension2.md)             | La interfaz IWiaUIExtension2 proporciona métodos que reemplazan la interfaz de usuario predeterminada proporcionada por el sistema por una interfaz de usuario personalizada y que proporcionan un icono de dispositivo personalizado. Los proveedores de dispositivos pueden implementar esta interfaz para proporcionar interfaces de usuario personalizadas para sus dispositivos.<br/>                                                                                                                                                                                                                     |



 

### <a name="new-and-changed-overviews-for-wia-20"></a>Información general nueva y modificada para WIA 2.0



| Tema                                                                          | Contenido |
|--------------------------------------------------------------------------------|----------|
| [Constantes](-wia-constants.md)                                                |          |
| [Funciones](-wia-functions.md)                                                |          |
| [Interfaces](-wia-interfaces.md)                                              |          |
| [Esquema de perfil de examen](-wia-scan-profile-schema.md)                            |          |
| [Estructuras](-wia-structures.md)                                              |          |
| [Transferencia de datos de imagen en WIA 2.0](-wia-transferring-image-data-in-wia2.md) |          |
| [Especificadores de tipo de dispositivo WIA](-wia-wia-device-type-specifiers.md)              |          |
| [Constantes de propiedad WIA](-wia-wia-property-constants.md)                      |          |



 

## <a name="leave-feedback"></a>Dejar comentarios

Correo electrónico para **sdkfdbk@microsoft.com** realizar informes de errores y solicitudes de características directamente a Microsoft.

 

 




