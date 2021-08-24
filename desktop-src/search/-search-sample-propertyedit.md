---
description: En el ejemplo de código PropertyEdit se muestra cómo convertir el nombre de propiedad canónica en PROPERTYKEY, establecer el valor del almacén de propiedades en el del elemento y volver a escribir los datos en la secuencia de archivos.
ms.assetid: 5918b4f6-6b6f-4229-8f29-1c41f80b3b02
title: PropertyEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944419f990c8f1f8b52706dbab0b08102829e77a5bfa8a91c72a5bc16eddfa63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944677"
---
# <a name="propertyedit"></a>PropertyEdit

En el ejemplo de código PropertyEdit se muestra cómo convertir el nombre de propiedad canónica en PROPERTYKEY, establecer el valor del almacén de propiedades en el del elemento y volver a escribir los datos en la secuencia de archivos.

En este tema se incluyen las siguientes secciones.

-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="requirements"></a>Requisitos



| Producto     | Versión mínima del producto |
|-------------|-------------------------|
| Windows     | Windows 7               |
| Windows SDK | 7,0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Ubicación      | Dirección URL de ruta de acceso                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub  | [Ejemplo propertyEdit](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/PropertyEdit)    |



 

 

> [!Note]  
> Para todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.

 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y vaya al directorio **del proyecto PropertyEdit.** 
2.  Escriba `msbuild PropertyEdit.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (opción preferida):

1.  Abra Windows Explorador de aplicaciones y vaya al directorio **del proyecto PropertyEdit.**
2.  Haga doble clic en el icono del archivo PropertyEdit.sln para abrir el proyecto en Visual Studio.
    > [!Note]  
    > La extensión de nombre de archivo .sln no se muestra en la configuración de carpeta predeterminada. En esa situación, se puede identificar por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".

     

3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Vaya al directorio que contiene el nuevo ejecutable, mediante la ventana símbolo del sistema o Windows explorador.
2.  En el símbolo del sistema, escriba `PropertyEdit.exe` o, en Windows Explorer, haga doble clic en el icono de PropertyEdit.exe.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
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

 

 
