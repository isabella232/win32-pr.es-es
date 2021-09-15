---
description: Describe cómo crear un controlador para las asignaciones de iconos personalizados.
ms.assetid: 23ed3a21-cf62-4440-b983-fae23aa56890
title: Cómo crear controladores de iconos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c620b6f6a4c05f8996a26c8365e4f4201ee0b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468205"
---
# <a name="how-to-create-icon-handlers"></a>Cómo crear controladores de iconos

Un [tipo de archivo](fa-file-types.md) a menudo tiene un icono personalizado asociado, para que sus miembros se puedan reconocer fácilmente en Windows Explorer. La manera más sencilla de asignar un icono personalizado a un tipo de archivo es registrar el archivo del icono. Sin embargo, un icono registrado de esta manera será el mismo para todos los miembros del tipo de archivo. Puede tener mucha más flexibilidad a la hora de asignar iconos a los miembros del tipo de archivo implementando un controlador *de iconos*.

Un controlador de iconos es un tipo de controlador de extensión de Shell que permite asignar iconos dinámicamente a los miembros de un tipo de archivo. Cada vez que se muestra un archivo del tipo, el Shell consulta al controlador para obtener el icono adecuado. Por ejemplo, un controlador de iconos puede asignar iconos diferentes a distintos miembros del tipo de archivo o variar el icono en función del estado actual del archivo.

Los procedimientos generales para implementar y registrar un controlador de extensión de Shell se de abordan en [Crear controladores de extensión de shell](handlers.md). Este documento se centra en los aspectos de implementación específicos de los controladores de iconos.

-   [Implementar controladores de iconos](#step-1-implementing-icon-handlers)
-   [Implementación de la interfaz IExtractIcon](#step-2-implementing-the-iextracticon-interface)
-   [Registrar controladores de iconos](#step-3-registering-icon-handlers)
-   [Temas relacionados](#related-topics)

## <a name="instructions"></a>Instructions

### <a name="step-1-implementing-icon-handlers"></a>Paso 1: Implementar controladores de iconos

Al igual que todos los controladores de extensión de Shell, los controladores de iconos son objetos del Modelo de objetos componentes (COM) en proceso implementados como archivos DLL. Deben exportar dos interfaces además de [**IUnknown:**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) e [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).

El shell inicializa el controlador a través de su [**interfaz IPersistFile.**](/windows/win32/api/objidl/nn-objidl-ipersistfile) Usa esta interfaz para solicitar el identificador de clase (CLSID) del controlador y le proporciona el nombre del archivo. El resto de la operación tiene lugar a través de [**la interfaz IExtractIcon.**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) Para obtener una explicación general de cómo implementar controladores de extensión de Shell, incluida la **interfaz IPersistFile,** vea [Creating Shell Extension Handlers](handlers.md). En el resto de este documento se describe cómo implementar la **interfaz IExtractIcon.**

### <a name="step-2-implementing-the-iextracticon-interface"></a>Paso 2: Implementar la interfaz IExtractIcon

Una vez inicializada la interfaz, el Shell usa la interfaz [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) del controlador para solicitar el icono adecuado. La interfaz tiene dos métodos: [**IExtractIcon::GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation) e [**IExtractIcon::Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract).

Los iconos se identifican por su ubicación en el sistema de archivos. Se [**llama al método IExtractIcon::GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation) para solicitar esta información. Establezca el *parámetro szIconFile* en el nombre de archivo. Si hay más de un icono en el archivo, establezca *piIndex* en el índice del icono. Asigne los valores adecuados a las dos variables de marca. Si no desea especificar un nombre de archivo, o si no desea que el shell extraiga el icono, establezca la marca **\_ NOTFILENAME deIVOS** en el *parámetro pwFlags.* No es necesario asignar un valor a *szIconFile*, pero el controlador debe proporcionar identificadores de icono cuando el shell llama a [**IExtractIcon::Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract).

Si devuelve un nombre de archivo, el Shell normalmente intenta cargar el icono desde su memoria caché. Para evitar la carga de un icono almacenado en caché, establezca la **marca \_ DONTCACHE de NILO** en el *parámetro pwFlags.* Si no se carga un icono almacenado en caché, el shell llama a [**IExtractIcon::Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract) para solicitar el identificador de icono.

Si [**IExtractIcon::GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation)especificó un archivo e índice, se pasan a [**IExtractIcon::Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract) en los parámetros *pszFile* y *nIconIndex,* respectivamente. Si se proporciona un nombre de archivo, el controlador puede devolver S \_ FALSE para que el shell extraiga el icono. De lo contrario, el controlador debe extraer o generar iconos grandes y pequeños, y asignar sus identificadores HICON a los parámetros *phiconLarge* y *phiconSmall.* El Shell agrega los iconos a su memoria caché para acelerar las llamadas posteriores al controlador.

### <a name="step-3-registering-icon-handlers"></a>Paso 3: Registrar controladores de iconos

Al registrar [estáticamente un icono para](icon.md) un tipo [de](fa-file-types.md)archivo , se crea una subclave **DefaultIcon** en el ProgID para el tipo de archivo. Su valor predeterminado se establece en el archivo que contiene el icono. Para registrar un controlador de iconos, debe tener la subclave **DefaultIcon,** pero su valor predeterminado debe establecerse en "%1". Agregue una subclave **IconHandler** a la subclave **Shellex** de la subclave ProgID y establezca su valor predeterminado en la forma de cadena del GUID de CLSID del controlador. Para obtener una explicación general de cómo registrar controladores de extensión de Shell, vea [Creating Shell Extension Handlers](handlers.md).

En el ejemplo siguiente se [](icon.md) modifica la entrada del Registro de Personalización de iconos para que el tipo de archivo .myp use ahora un controlador de menú contextual en lugar de un icono definido estáticamente.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      DefaultIcon
         (Default) = %1
      Shellex
         IconHandler
            (Default) = {The handler's CLSID GUID}
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de controladores de extensiones de shell](handlers.md)
</dt> <dt>

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)
</dt> </dl>

 

 
