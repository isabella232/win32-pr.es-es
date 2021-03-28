---
description: En este tema se explica cómo registrar un controlador de vista previa asociado a un tipo de datos determinado.
ms.assetid: 5f194d29-d09f-4426-a63e-911db65ce700
title: Cómo registrar un controlador de vista previa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5af9610de1822678521557fc20aa53f4e556e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985419"
---
# <a name="how-to-register-a-preview-handler"></a>Cómo registrar un controlador de vista previa

En este tema se explica cómo registrar un controlador de vista previa asociado a un tipo de datos determinado. Para los fines de la ilustración, en los ejemplos de este tema se usa un tipo de archivo. XYZ. El registro de un controlador de vista previa es un registro estándar basado en asociaciones de archivos.

## <a name="instructions"></a>Instrucciones

### <a name="step-1"></a>Paso 1:

En primer lugar, una extensión de nombre de archivo está asociada a un ProgID. La entrada siguiente asocia la subclave **xyzfile** ProgID con la extensión de nombre de archivo. XYZ.

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = [REG_SZ] xyzfile
```

La subclave **xyzfile** ProgID se almacena con los otros ProgID, tal como se muestra aquí:

```
HKEY_CLASSES_ROOT
   xyzfile
```

Cada subclave ProgID del controlador de vista previa contiene una subclave denominada **shellex** que contiene una subclave denominada *siempre* **{8895b1c6-b41f-4c1c-a562-0d564250836f}**. La presencia de esa subclave indica al sistema que el controlador es un controlador de vista previa.

El valor predeterminado de la subclave **{8895b1c6-b41f-4c1c-a562-0d564250836f}** es el identificador de clase (CLSID) del controlador. Aquí se muestra un ejemplo de la subclave **xyzfile** ProgID, que asocia un controlador de CLSID {ec3a629a-a47c-4245-bc78-b4b63d0e3154}.

```
HKEY_CLASSES_ROOT
   xyzfile
      shellex
         {8895b1c6-b41f-4c1c-a562-0d564250836f}
            (Default) = [REG_SZ] {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
```

### <a name="step-2"></a>Paso 2:

A continuación, agregue la subclave en **CLSID** para el controlador de vista previa. Aquí se muestra un ejemplo. A continuación se ofrece una explicación de las entradas individuales.

```
HKEY_CLASSES_ROOT
   CLSID
      {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
         (Default) = [REG_SZ] Fabricam XYZ Preview Handler
         DisplayName = [REG_SZ] @myhandler.dll,-101
         Icon = [REG_SZ] myhandler.dll,201
         AppID = [REG_SZ] {6d2b5079-2f0b-48dd-ab7f-97cec514d30b}
         InprocServer32
            (Default) = [REG_EXPAND_SZ] %ProgramFiles%\Fabricam\myhandler.dll
            ThreadingModel = [REG_SZ] Apartment
            ProgID = [REG_SZ] xyzfile
            VersionIndependentProgID = [REG_SZ] Version IndependentProgID
```

El valor predeterminado de la subclave (aquí, **{ec3a629a-a47c-4245-bc78-b4b63d0e3154}**) no es necesario ni se usa. Sin embargo, establecerlo en una cadena no localizada puede ayudarle a depurar problemas de registro.

El signo menos (-101) del recurso. dll de la entrada DisplayName existe por motivos de herencia. La entrada del icono, por otro lado, no requiere un signo menos.

El valor de AppID proporciona una referencia al AppID de la aplicación asociada a la extensión de nombre de archivo (almacenada en **HKEY \_ clases \_ raíz** \\ **AppID**. El valor que se usa aquí ({6d2b5079-2f0b-48dd-ab7f-97cec514d30b}) es el identificador del host suplente Prevhost.exe. los controladores de vista previa de bits de 32 deben usar **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} cuando se instalan en sistemas operativos de 64 bits.

Las entradas bajo la subclave **InProcServer32** incluyen una referencia a la subclave ProgID de la extensión de nombre de archivo, así como una entrada para un [VersionIndependentProgID](../com/versionindependentprogid.md).

### <a name="step-3"></a>Paso 3:

Por último, el controlador de vista previa se debe agregar a la lista de todos los controladores de vista previa. El sistema usa esta lista como una optimización para enumerar todos los controladores de vista previa registrados con fines de visualización. De nuevo, el valor predeterminado no es necesario, simplemente contribuye al proceso de depuración.

> [!Note]  
> En Windows 7, si la aplicación está instalada para todos los usuarios del equipo, use HKEY \_ local \_ Machine; si solo hay un usuario, use HKEY \_ Current \_ User.

 

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PreviewHandlers
                  {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
                     (Default) = [REG_SZ] Fabricam XYZ Preview Handler
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controladores de vista previa y host de vista previa de Shell](preview-handlers.md)
</dt> <dt>

[Crear controladores de vista previa](building-preview-handlers.md)
</dt> <dt>

[Instrucciones de controlador de vista previa](preview-handler-guidelines.md)
</dt> </dl>

 

 
