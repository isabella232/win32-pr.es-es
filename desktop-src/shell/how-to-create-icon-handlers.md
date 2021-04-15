---
description: Describe cómo crear un controlador para asignaciones de iconos personalizadas.
ms.assetid: 23ed3a21-cf62-4440-b983-fae23aa56890
title: Cómo crear controladores de iconos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c620b6f6a4c05f8996a26c8365e4f4201ee0b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985459"
---
# <a name="how-to-create-icon-handlers"></a>Cómo crear controladores de iconos

A menudo, un [tipo de archivo](fa-file-types.md) tiene un icono personalizado asociado a él para que sus miembros sean fácilmente reconocibles en el explorador de Windows. La manera más sencilla de asignar un icono personalizado a un tipo de archivo es registrar el archivo del icono. Sin embargo, un icono registrado de este modo será el mismo para todos los miembros del tipo de archivo. Puede tener mucha más flexibilidad a la hora de asignar iconos a los miembros del tipo de archivo implementando un *controlador de icono*.

Un controlador de icono es un tipo de controlador de extensión de Shell que permite asignar de forma dinámica iconos a los miembros de un tipo de archivo. Cada vez que se muestra un archivo del tipo, el shell consulta el icono correspondiente al controlador. Por ejemplo, un controlador de iconos puede asignar iconos diferentes a los distintos miembros del tipo de archivo o variar el icono en función del estado actual del archivo.

Los procedimientos generales para implementar y registrar un controlador de extensión de Shell se explican en [crear controladores de extensión de Shell](handlers.md). Este documento se centra en los aspectos de la implementación que son específicos de los controladores de iconos.

-   [Implementar controladores de iconos](#step-1-implementing-icon-handlers)
-   [Implementar la interfaz IExtractIcon](#step-2-implementing-the-iextracticon-interface)
-   [Registrar controladores de iconos](#step-3-registering-icon-handlers)
-   [Temas relacionados](#related-topics)

## <a name="instructions"></a>Instrucciones

### <a name="step-1-implementing-icon-handlers"></a>Paso 1: implementar controladores de iconos

Al igual que todos los controladores de extensión de Shell, los controladores de iconos son objetos de modelo de objetos componentes (COM) en proceso implementados como archivos dll. Deben exportar dos interfaces además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) y [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).

El shell inicializa el controlador a través de su interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) . Utiliza esta interfaz para solicitar el identificador de clase (CLSID) del controlador y proporciona el nombre del archivo. El resto de la operación se lleva a cabo a través de la interfaz [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) . Para obtener información general sobre cómo implementar controladores de extensión de Shell, incluida la interfaz **IPersistFile** , vea [crear controladores de extensión de Shell](handlers.md). En el resto de este documento se explica cómo implementar la interfaz **IExtractIcon** .

### <a name="step-2-implementing-the-iextracticon-interface"></a>Paso 2: implementación de la interfaz IExtractIcon

Una vez inicializada la interfaz, el shell usa la interfaz [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) del controlador para solicitar el icono adecuado. La interfaz tiene dos métodos: [**IExtractIcon:: GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation) y [**IExtractIcon:: Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract).

Los iconos se identifican por su ubicación en el sistema de archivos. Se llama al método [**IExtractIcon:: GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation) para solicitar esta información. Establezca el parámetro *szIconFile* en el nombre de archivo. Si hay más de un icono en el archivo, establezca *piIndex* en el índice del icono. Asigne los valores adecuados a las dos variables de marca. Si no desea especificar un nombre de archivo o si no desea que el shell Extraiga el icono, establezca la marca **Gil \_ NOTFILENAME** en el parámetro *pwFlags* . No es necesario asignar un valor a *szIconFile*, pero el controlador debe proporcionar los identificadores de icono cuando el shell llama a [**IExtractIcon:: Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract).

Si devuelve un nombre de archivo, el shell normalmente intenta cargar el icono desde su memoria caché. Para evitar la carga de un icono almacenado en caché, establezca la marca **Gil \_ DONTCACHE** en el parámetro *pwFlags* . Si no se carga un icono almacenado en caché, el shell llama a [**IExtractIcon:: Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract) para solicitar el identificador de icono.

Si [**IExtractIcon:: GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation)especifica un archivo e índice, se pasan a [**IExtractIcon:: Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract) en los parámetros *pszFile* y *nIconIndex* , respectivamente. Si se proporciona un nombre de archivo, el controlador puede devolver S \_ false para que el shell Extraiga el icono. De lo contrario, el controlador debe extraer o producir iconos grandes y pequeños, y asignar sus identificadores de HICON a los parámetros *phiconLarge* y *phiconSmall* . El shell agrega los iconos a su memoria caché para agilizar las llamadas posteriores al controlador.

### <a name="step-3-registering-icon-handlers"></a>Paso 3: registrar controladores de iconos

Al [registrar estáticamente un icono](icon.md) para un [tipo de archivo](fa-file-types.md), se crea una subclave **DefaultIcon** en el identificador de programa (ProgID) para el tipo de archivo. Su valor predeterminado se establece en el archivo que contiene el icono. Para registrar un controlador de iconos, debe tener todavía la subclave **DefaultIcon** , pero su valor predeterminado debe establecerse en "%1". Agregue una subclave **IconHandler** a la subclave **Shellex** de la subclave ProgID y establezca su valor predeterminado en la forma de cadena del GUID CLSID del controlador. Para obtener información general sobre cómo registrar controladores de extensión de Shell, vea [crear controladores de extensión de Shell](handlers.md).

En el ejemplo siguiente se modifica la entrada del registro desde la [Personalización de iconos](icon.md) para que el tipo de archivo. MYP ahora use un controlador de menú contextual en lugar de un icono definido estáticamente.

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

 

 
