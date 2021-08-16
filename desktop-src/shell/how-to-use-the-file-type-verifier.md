---
description: En este tema se describe cómo usar el comprobador de tipos de archivo que se proporciona en el SDK Windows 7.
ms.assetid: 96FCA74B-DEB2-49D1-B670-EBD8BE0783F1
title: Cómo usar el comprobador de tipos de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65af06de30d4fca2a9f5209d20e200153c061248576e7e94c8342cf9ae60e4f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223377"
---
# <a name="how-to-use-the-file-type-verifier"></a>Cómo usar el comprobador de tipos de archivo

En este tema se describe cómo usar el comprobador de tipos de archivo que se proporciona en el [SDK Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Si el programa crea tipos de archivo con los que se espera que los usuarios interactúen desde el shell de Windows (normalmente almacenados en la carpeta conocida de un usuario, como **Mis documentos**), es muy importante probar la aplicación y comprobar que los archivos que crea están registrados correctamente y proporcionar una experiencia de usuario de alta calidad al examinar y buscar archivos. Esto es especialmente importante si espera que los usuarios ejecuten las aplicaciones en Windows 7, que se basa en controladores de tipo de archivo de alta calidad para muchas de las características de Shell.

Para comprobar el tipo de archivo mediante el comprobador de tipos de archivo, siga estos pasos.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Paso 1:

Instale la aplicación en el entorno de prueba y copie el comprobador de tipo de archivo en ese entorno. El comprobador de tipos de archivo está disponible en [el SDK Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

### <a name="step-2"></a>Paso 2:

Use la aplicación para crear un archivo que se va a probar.

### <a name="step-3"></a>Paso 3:

Inicie el comprobador de tipo de archivo.

### <a name="step-4"></a>Paso 4:

Seleccione la categoría del tipo de archivo, como se muestra en la siguiente captura de pantalla.

![Captura de pantalla que muestra la función de arrastrar y colocar.](images/file-assoc/filetypeverifier1.png)

La selección de categorías determina el conjunto de pruebas que ejecutará la herramienta. Si el tipo podría estar en más de una categoría (por ejemplo, un archivo TIF podría ser una imagen o un documento en función del contenido), vuelva a ejecutar la herramienta con cada categoría adecuada.

### <a name="step-5"></a>Paso 5:

Mediante Windows Explorador de archivos, busque un archivo que se va a probar y use el mouse para arrastrarlo al destino en File Type Verifier ( Comprobador de tipo de archivo), como se muestra en la siguiente captura de pantalla.

![captura de pantalla que muestra la función de arrastrar y colocar](images/file-assoc/filetypeverifier2.png)

### <a name="step-6"></a>Paso 6:

Espere a que la herramienta File Type Verifier continúe con una serie de pruebas. El progreso de las pruebas se muestra en la barra de progreso, como en la siguiente captura de pantalla.

![captura de pantalla que muestra la barra de progreso](images/file-assoc/filetypeverifier3.png)

### <a name="step-7"></a>Paso 7:

Revise el resumen de resultados de las pruebas de tipo de archivo de documento, como se muestra en la siguiente captura de pantalla.

![captura de pantalla que muestra el resumen de los resultados](images/file-assoc/filetypeverifier4.png)

### <a name="step-8"></a>Paso 8:

Haga clic en cualquiera de los resultados de la página de resumen para ver el registro detallado. En la siguiente captura de pantalla se muestra un registro de ejemplo para un controlador de vista previa.

![captura de pantalla que muestra el registro del controlador de vista previa](images/file-assoc/filetypeverifier5.png)

### <a name="step-9"></a>Paso 9:

Para guardar una copia del  archivo de registro, haga clic en Guardar archivo de registro en la parte inferior de la pantalla del registro y elija una ubicación adecuada para almacenarlo en el equipo.

### <a name="step-10"></a>Paso 10:

Si se notifican errores, realice los cambios adecuados en la aplicación y vuelva a ejecutar la herramienta para comprobar que los errores ya no aparecen en las pruebas. Si se notifican advertencias, evalúelas y decida si son pertinentes para el tipo de archivo concreto y realice los cambios adecuados en la aplicación según sea necesario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[SDK de Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
</dt> </dl>

 

 



