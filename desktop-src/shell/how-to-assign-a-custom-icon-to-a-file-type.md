---
description: Se debe asignar un icono personalizado a un tipo de archivo para proporcionar una indicación visual al usuario de ese tipo de archivo o a la aplicación a la que está asociado el tipo de archivo.
ms.assetid: 84F293C2-BAB1-4BF8-9F89-122B6DAB29C3
title: Cómo asignar un icono personalizado a un tipo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf625eb6177471702096f462846b8035772177ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985470"
---
# <a name="how-to-assign-a-custom-icon-to-a-file-type"></a>Cómo asignar un icono personalizado a un tipo de archivo

Cuando no se asigna ningún icono predeterminado personalizado a un tipo de archivo, el escritorio y el explorador de Windows muestran todos los archivos de ese tipo con un icono predeterminado genérico. Por ejemplo, en la siguiente captura de pantalla se muestra este icono predeterminado que se usa con el archivo MyDocs4. MYP.

![captura de pantalla del icono predeterminado](images/icon.png)

Aunque todos los archivos que se muestran en esta captura de pantalla son archivos de texto simples, solo MyDocs4. MYP muestra el icono predeterminado de Windows. Esto se debe a que la extensión. txt es un tipo de archivo registrado que tiene un icono predeterminado personalizado.

En la captura de pantalla siguiente se muestra un icono personalizado que se ha asignado al tipo de archivo. MYP.

![captura de pantalla del icono personalizado para los archivos. MYP](images/context4.png)

> [!Note]  
> Los iconos también se pueden asignar de acuerdo con una aplicación específica.

 

## <a name="instructions"></a>Instrucciones

### <a name="step-1"></a>Paso 1:

Cree una subclave denominada **DefaultIcon** en una de las dos ubicaciones siguientes:

-   Para una asignación de tipo de archivo **, \_ clases HKEY \_ raíz** \\ *. Extension*
-   Para una asignación de aplicación **, \_ clases HKEY \_ raíz** \\ *ProgID*

### <a name="step-2"></a>Paso 2:

Asigne a la subclave **DefaultIcon** un valor predeterminado de tipo **reg \_ SZ** que especifique la ruta de acceso completa del archivo que contiene el icono.

### <a name="step-3"></a>Paso 3:

Llame a la función [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) para notificar al shell que actualice su caché de iconos.

## <a name="remarks"></a>Observaciones

En el ejemplo siguiente se muestra una vista detallada de las entradas del registro necesarias para una asignación de icono de tipo de archivo. La extensión de nombre de archivo está asociada a una aplicación, pero la asignación de icono es a la propia extensión de nombre de archivo, por lo que la aplicación asociada no dicta el icono predeterminado.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

En el ejemplo siguiente se muestra una vista detallada de las entradas del registro necesarias para la asignación de un icono de aplicación. La extensión de nombre de archivo. MYP se asocia primero a la aplicación de mi programa. 1. A continuación, se asigna a la subclave de PROG. 1 ProgID el icono predeterminado personalizado.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

Cualquier archivo que contenga un icono es aceptable, incluidos los archivos. ico,. exe y. dll. Si hay más de un icono en el archivo, la ruta de acceso debe ir seguida de una coma y, a continuación, el índice del icono.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de archivo](fa-file-types.md)
</dt> </dl>

 

 



