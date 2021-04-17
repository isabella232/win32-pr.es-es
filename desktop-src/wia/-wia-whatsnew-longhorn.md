---
description: En la adquisición de imágenes de Windows (WIA) 2,0 se incluyen muchas nuevas API de adquisición de imágenes de Windows (WIA).
ms.assetid: d8e85c34-d8ce-4512-af71-102a21393fdf
title: Novedades de la adquisición de imágenes de Windows (WIA) 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f9d225185b8f1ff2d6441a7ddf0e8fd919ac98
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105697984"
---
# <a name="whats-new-in-windows-image-acquisition-wia-20"></a>Novedades de la adquisición de imágenes de Windows (WIA) 2,0

En la adquisición de imágenes de Windows (WIA) 2,0 se incluyen muchas nuevas API de adquisición de imágenes de Windows (WIA). Además, hay algunas incompatibilidades con versiones anteriores y posteriores entre la adquisición de imágenes de Windows (WIA) 1,0 y el servicio WIA 2,0 que se incluye con Windows Vista. Algunas interfaces, estructuras, propiedades y valores de propiedad de WIA 1,0 no son compatibles con, y las aplicaciones que las usan no se ejecutan en, Windows Vista y versiones posteriores. Del mismo modo, las aplicaciones que usan las nuevas interfaces, estructuras, propiedades y valores de propiedad introducidos con WIA 2,0 (vea más abajo) no se ejecutarán en versiones del sistema operativo anteriores a Windows Vista.

## <a name="new-api-for-wia-20"></a>Nueva API para WIA 2,0

### <a name="constants-lists-updated-for-wia-20"></a>Constantes: listas actualizadas para WIA 2,0

-   [**Constantes comunes de propiedades de elementos WIA**](-wia-wiaitempropcommonitem.md)
-   [**Constantes de propiedades de información del dispositivo**](-wia-wiadeviceinfoprop.md)
-   [**Constantes de propiedades de dispositivo de escáner**](-wia-wiaitempropscannerdevice.md)
-   [**Constantes de propiedad del elemento WIA del escáner**](-wia-wiaitempropscanneritem.md)
-   [**GUID de categoría de elemento de WIA 2,0**](-wia-wia2-itemcategoryguids.md)
-   [**Constantes de tamaño de página de WIA 2,0**](-wia-wia2-pagesizeconstants.md)
-   [**Marcas de tipo de elemento WIA**](-wia-wia-item-type-flags.md)

### <a name="new-structures-in-wia-20"></a>Nuevas estructuras en WIA 2,0



| Tema                                               | Contenido                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) | Define los datos necesarios para llamar a un cuadro de diálogo de dispositivo.<br/>                                                                                                                                                                                                       |
| [**encabezado de WIA \_ sin formato \_**](-wia-wia-raw-header.md)     | La estructura de [**\_ \_ encabezado sin formato de WIA**](-wia-wia-raw-header.md) define una imagen en el formato de datos sin procesar de un dispositivo y permite a las aplicaciones usar el formato sin formato en las transferencias de WIA.<br/>                                                                         |
| [**WiaTransferParams**](-wia-wiatransferparams.md) | El sistema en tiempo de ejecución de WIA transmite el [**WiaTransferParams**](-wia-wiatransferparams.md) a una aplicación durante una transferencia de datos al método [**IWiaTransferCallback:: TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) .<br/> |



 

### <a name="new-interfaces-in-wia-20"></a>Nuevas interfaces en WIA 2,0



| Tema                                                         | Contenido                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)                   | Lo usan las aplicaciones para enumerar los objetos [**IWiaItem2**](-wia-iwiaitem2.md) en la carpeta actual del árbol de elementos.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**IScanProfile**](-wia-iscanprofile.md)                     | La interfaz [**IScanProfile**](-wia-iscanprofile.md) representa un único Perfil de examen y permite a las aplicaciones establecer y obtener las propiedades del perfil. <br/>                                                                                                                                                                                                                                                                                                                                   |
| [**IScanProfileMgr**](-wia-iscanprofilemgr.md)               | La interfaz [**IScanProfileMgr**](-wia-iscanprofilemgr.md) proporciona métodos para crear, abrir, eliminar y administrar perfiles de digitalización. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**IScanProfileUI**](-wia-iscanprofileui.md)                 | La interfaz [**IScanProfileUI**](-wia-iscanprofileui.md) permite a las aplicaciones mostrar un cuadro de diálogo para que los usuarios puedan crear, modificar y eliminar perfiles de digitalización.<br/>                                                                                                                                                                                                                                                                                                                               |
| [**IWiaAppErrorHandler**](-wia-iwiaapperrorhandler.md)       | La interfaz [**IWiaAppErrorHandler**](-wia-iwiaapperrorhandler.md) permite a las aplicaciones mostrar ventanas de errores (durante las transferencias de datos) desde las que el usuario puede elegir si desea continuar, cancelar o anular la transferencia.<br/>                                                                                                                                                                                                                                                                     |
| [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)                       | La interfaz [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) se usa para crear y administrar dispositivos de adquisición de imágenes y registrarse para recibir eventos de dispositivo.<br/>                                                                                                                                                                                                                                                                                                                                             |
| [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md)             | La interfaz [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md) proporciona métodos para controlar los errores que pueden producirse cuando una aplicación solicita datos de imagen, ya sea para los bits de vista previa o final. <br/>                                                                                                                                                                                                                                                                                                      |
| [**IWiaImageFilter**](-wia-iwiaimagefilter.md)               | La interfaz [**IWiaImageFilter**](-wia-iwiaimagefilter.md) es una interfaz de extensión implementada por los desarrolladores de filtros de procesamiento de imágenes y que WIA 2,0 llama. <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**IWiaItem2**](-wia-iwiaitem2.md)                           | La interfaz [**IWiaItem2**](-wia-iwiaitem2.md) proporciona a las aplicaciones la misma funcionalidad que la interfaz [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (la capacidad de consultar dispositivos para detectar sus capacidades, tener acceso a las interfaces de transferencia de datos y las propiedades de los elementos, y para controlar el dispositivo). También proporciona a las aplicaciones la capacidad de crear y usar de forma dinámica filtros de procesamiento de imágenes que pueden ser extensiones de los controladores de dispositivos WIA 2,0 proporcionados en Windows Vista.<br/> |
| [**IWiaPreview**](-wia-iwiapreview.md)                       | La interfaz [**IWiaPreview**](-wia-iwiapreview.md) almacena en caché las imágenes sin filtrar internamente y las pasa a través de filtros de procesamiento de imágenes. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md) | La interfaz [**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md) detecta subregiones de una secuencia de imágenes y crea elementos [**IWiaItem2**](-wia-iwiaitem2.md) independientes para cada una de ellas. <br/>                                                                                                                                                                                                                                                                                                         |
| [**IWiaTransfer**](-wia-iwiatransfer.md)                     | La interfaz [**IWiaTransfer**](-wia-iwiatransfer.md) proporciona transferencia de datos basada en secuencias. <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**IWiaTransferCallback**](-wia-iwiatransfercallback.md)     | La interfaz [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) recibe las devoluciones de llamada durante una transferencia de datos. <br/>                                                                                                                                                                                                                                                                                                                                                                                |
| [**IWiaUIExtension2**](-wia-iwiauiextension2.md)             | La interfaz IWiaUIExtension2 proporciona métodos que reemplazan la interfaz de usuario predeterminada proporcionada por el sistema por una interfaz de usuario personalizada y que proporcionan un icono de dispositivo personalizado. Los proveedores de dispositivos pueden implementar esta interfaz para proporcionar interfaces de usuario personalizadas para sus dispositivos.<br/>                                                                                                                                                                                                                     |



 

### <a name="new-and-changed-overviews-for-wia-20"></a>Información general nueva y modificada para WIA 2,0



| Tema                                                                          | Contenido |
|--------------------------------------------------------------------------------|----------|
| [Constantes](-wia-constants.md)                                                |          |
| [Funciones](-wia-functions.md)                                                |          |
| [Interfaces](-wia-interfaces.md)                                              |          |
| [Esquema de análisis de perfil](-wia-scan-profile-schema.md)                            |          |
| [Estructuras](-wia-structures.md)                                              |          |
| [Transferir datos de imagen en WIA 2,0](-wia-transferring-image-data-in-wia2.md) |          |
| [Especificadores de tipo de dispositivo WIA](-wia-wia-device-type-specifiers.md)              |          |
| [Constantes de propiedad de WIA](-wia-wia-property-constants.md)                      |          |



 

## <a name="leave-feedback"></a>Dejar comentarios

Correo electrónico **sdkfdbk@microsoft.com** para crear informes de errores y solicitudes de características directamente a Microsoft.

 

 




