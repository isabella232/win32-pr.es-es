---
description: En este tema se describe cómo usar el comprobador de tipo de archivo que se proporciona en el SDK de Windows 7.
ms.assetid: 96FCA74B-DEB2-49D1-B670-EBD8BE0783F1
title: Cómo usar el comprobador de tipo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f083897499f972f945867a0c02318df192e734d9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "104279697"
---
# <a name="how-to-use-the-file-type-verifier"></a>Cómo usar el comprobador de tipo de archivo

En este tema se describe cómo usar el comprobador de tipo de archivo que se proporciona en el [SDK de Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Si el programa crea tipos de archivos con los que se espera que los usuarios interactúen desde el shell de Windows (normalmente almacenado en la carpeta conocida de un usuario, como **Mis documentos**), es muy importante probar la aplicación y comprobar que los archivos que crea están correctamente registrados y proporcionar una experiencia de usuario de alta calidad al examinar y buscar archivos. Esto es especialmente importante si espera que los usuarios ejecuten sus aplicaciones en Windows 7, que se basa en controladores de tipo de archivo de alta calidad para muchas de las características de Shell.

Para comprobar el tipo de archivo mediante el comprobador de tipo de archivo, siga estos pasos.

## <a name="instructions"></a>Instrucciones

### <a name="step-1"></a>Paso 1:

Instale la aplicación en el entorno de prueba y copie el comprobador de tipo de archivo en ese entorno. El comprobador de tipo de archivo está disponible en el [SDK de Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

### <a name="step-2"></a>Paso 2:

Use la aplicación para crear un archivo que se va a probar.

### <a name="step-3"></a>Paso 3:

Inicie el comprobador de tipo de archivo.

### <a name="step-4"></a>Paso 4:

Seleccione la categoría del tipo de archivo, tal y como se muestra en la siguiente captura de pantalla.

![Captura de pantalla que muestra la función de arrastrar y colocar.](images/file-assoc/filetypeverifier1.png)

La selección de categoría determina el conjunto de pruebas que ejecutará la herramienta. Si el tipo puede estar por debajo de más de una categoría (por ejemplo, un archivo TIF puede ser una imagen o un documento en función del contenido), vuelva a ejecutar la herramienta con cada categoría adecuada.

### <a name="step-5"></a>Paso 5:

Con el explorador de Windows, busque un archivo que se va a probar y use el mouse para arrastrarlo al destino en el comprobador de tipo de archivo, como se muestra en la siguiente captura de pantalla.

![captura de pantalla que muestra la función de arrastrar y colocar](images/file-assoc/filetypeverifier2.png)

### <a name="step-6"></a>Paso 6:

Espere a que la herramienta Comprobador de tipo de archivo continúe a través de una serie de pruebas. La barra de progreso muestra el progreso de las pruebas, como en la siguiente captura de pantalla.

![captura de pantalla que muestra la barra de progreso](images/file-assoc/filetypeverifier3.png)

### <a name="step-7"></a>Paso 7:

Revise el Resumen de resultados de las pruebas de tipo de archivo de documento, tal y como se muestra en la siguiente captura de pantalla.

![captura de pantalla que muestra el Resumen de resultados](images/file-assoc/filetypeverifier4.png)

### <a name="step-8"></a>Paso 8:

Haga clic en cualquiera de los resultados de la página Resumen para ver el registro detallado. En la captura de pantalla siguiente se muestra un registro de ejemplo para un controlador de vista previa.

![captura de pantalla que muestra el registro del controlador de vista previa](images/file-assoc/filetypeverifier5.png)

### <a name="step-9"></a>Paso 9:

Para guardar una copia del archivo de registro, haga clic en **Guardar archivo de registro** en la parte inferior de la pantalla del registro y elija una ubicación adecuada para almacenarlo en el equipo.

### <a name="step-10"></a>Paso 10:

Si se detectan errores, realice los cambios apropiados en la aplicación y vuelva a ejecutar la herramienta para comprobar que los errores ya no se muestran en las pruebas. Si se registran las advertencias, evalúelos y decida si son relevantes para su tipo de archivo concreto y realice los cambios apropiados en la aplicación según sea necesario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[SDK de Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
</dt> </dl>

 

 



