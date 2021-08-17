---
description: Se debe asignar un icono personalizado a un tipo de archivo para proporcionar una indicación visual al usuario de ese tipo de archivo o a la aplicación a la que está asociado el tipo de archivo.
ms.assetid: 84F293C2-BAB1-4BF8-9F89-122B6DAB29C3
title: Asignación de un icono personalizado a un tipo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d156322bfe0899ed48c6c27f2660b911d9e5c77791c550b6141144d95384b6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119093009"
---
# <a name="how-to-assign-a-custom-icon-to-a-file-type"></a>Asignación de un icono personalizado a un tipo de archivo

Cuando no se asigna ningún icono predeterminado personalizado a un tipo de archivo, el escritorio y Windows Explorer muestran todos los archivos de ese tipo con un icono predeterminado genérico. Por ejemplo, la siguiente captura de pantalla muestra este icono predeterminado que se usa con el archivo MyDocs4.myp.

![captura de pantalla del icono predeterminado](images/icon.png)

Aunque todos los archivos que se muestran en esta captura de pantalla son archivos de texto simples, solo MyDocs4.myp muestra Windows icono predeterminado. Esto se debe a que la .txt es un tipo de archivo registrado que tiene un icono predeterminado personalizado.

En la captura de pantalla siguiente se muestra un icono personalizado que se ha asignado al tipo de archivo .myp.

![captura de pantalla del icono personalizado para archivos .myp](images/context4.png)

> [!Note]  
> Los iconos también se pueden asignar en función de la aplicación.

 

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Paso 1:

Cree una subclave **denominada DefaultIcon** en una de las dos ubicaciones siguientes:

-   Para una asignación de tipo de archivo, **HKEY \_ CLASSES \_ ROOT** \\ *.extension*
-   Para una asignación de aplicación, **HKEY \_ CLASSES \_ ROOT** \\ *ProgID*

### <a name="step-2"></a>Paso 2:

Asigne a la subclave **DefaultIcon** un valor predeterminado de tipo **REG \_ SZ** que especifique la ruta de acceso completa para el archivo que contiene el icono.

### <a name="step-3"></a>Paso 3:

Llame a [**la función SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) para notificar al Shell que actualice su caché de iconos.

## <a name="remarks"></a>Comentarios

En el ejemplo siguiente se muestra una vista detallada de las entradas del Registro necesarias para una asignación de icono de tipo de archivo. La extensión de nombre de archivo está asociada a una aplicación, pero la asignación de icono es a la propia extensión de nombre de archivo para que la aplicación asociada no dicta el icono predeterminado.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

En el ejemplo siguiente se muestra una vista detallada de las entradas del Registro necesarias para una asignación de icono de aplicación. La extensión de nombre de archivo .myp se asocia primero a la aplicación MyProgram.1. A continuación, se asigna el icono predeterminado personalizado a la subclave MyProgram.1 ProgID.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

Cualquier archivo que contenga un icono es aceptable, incluidos los archivos .ico, .exe y .dll. Si hay más de un icono en el archivo, la ruta de acceso debe ir seguida de una coma y, a continuación, el índice del icono.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de archivo](fa-file-types.md)
</dt> </dl>

 

 



