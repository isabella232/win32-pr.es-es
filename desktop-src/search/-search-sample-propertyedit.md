---
description: En el ejemplo de código PropertyEdit se muestra cómo convertir el nombre de la propiedad canónica en una PROPERTYKEY, establecer el valor del almacén de propiedades en el del elemento y volver a escribir los datos en la secuencia de archivos.
ms.assetid: 5918b4f6-6b6f-4229-8f29-1c41f80b3b02
title: PropertyEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa248b9e86f8ab93cccba3d5d6b169d7e8699dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907749"
---
# <a name="propertyedit"></a>PropertyEdit

En el ejemplo de código PropertyEdit se muestra cómo convertir el nombre de la propiedad canónica en una PROPERTYKEY, establecer el valor del almacén de propiedades en el del elemento y volver a escribir los datos en la secuencia de archivos.

En este tema se incluyen las siguientes secciones.

-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="requirements"></a>Requisitos



| Producto     | Versión mínima del producto |
|-------------|-------------------------|
| Windows     | Windows 7               |
| Windows SDK | 7.0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location      | URL de ruta de acceso                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub  | [Ejemplo de PropertyEdit](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/PropertyEdit)    |



 

 

> [!Note]  
> En todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.

 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **PropertyEdit** . 
2.  Escriba `msbuild PropertyEdit.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra el explorador de Windows y navegue hasta el directorio del proyecto **PropertyEdit** .
2.  Haga doble clic en el icono del archivo PropertyEdit. sln para abrir el proyecto en Visual Studio.
    > [!Note]  
    > La extensión de nombre de archivo. sln no se muestra en configuración de carpeta predeterminada. En esa situación, puede identificarse por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".

     

3.  En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Desplácese hasta el directorio que contiene el nuevo ejecutable, mediante la ventana del símbolo del sistema o el explorador de Windows.
2.  En el símbolo del sistema, escriba `PropertyEdit.exe` o, en el explorador de Windows, haga doble clic en el icono de PropertyEdit.exe.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Ejemplos de código de búsqueda](-search-samples-ovw.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> <dt>

[Acerca de las propiedades y los controladores de propiedades](../properties/building-property-handlers-properties.md)
</dt> <dt>

[Esquema de descripción de propiedad](/previous-versions//cc144127(v=vs.85))
</dt> </dl>

 

 
