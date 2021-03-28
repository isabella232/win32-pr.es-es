---
description: En Windows 7 y versiones posteriores, puede usar la subclave ExtendedSubCommandsKey para crear menús en cascada ampliados.
ms.assetid: 6E8B4FB7-D4DB-4DBC-AF6F-59D02CB6AB13
title: Crear menús en cascada con la entrada del registro ExtendedSubCommandsKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220a38825ae250a0d58d30bc7de93f290f819eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813710"
---
# <a name="how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a>Cómo crear menús en cascada con la entrada del registro ExtendedSubCommandsKey

En Windows 7 y versiones posteriores, puede usar la subclave **ExtendedSubCommandsKey** para crear menús en cascada ampliados.

La siguiente captura de pantalla es un ejemplo de un menú en cascada extendido.

![captura de pantalla que muestra el menú en cascada ampliado para dispositivos](images/file-assoc/extendedsubcommandskey.png)

Dado que la **\_ \_ raíz de las clases HKEY** es una combinación de **HKEY \_ Current \_ User** y **HKEY \_ local \_ Machine**, puede registrar los subverbos en la subclave de clases de software del **\_ \_ usuario actual HKEY** \\  \\  . La ventaja de hacerlo es que el permiso elevado no es necesario. Otras asociaciones de archivo pueden volver a usar todo el conjunto de verbos especificando la misma subclave **ExtendedSubCommandsKey** . Si no necesita volver a usar este conjunto de verbos, puede enumerar los verbos en el elemento primario. En este caso, asegúrese de que el valor predeterminado del elemento primario está vacío, tal como se muestra en el ejemplo de entrada del registro de esta sección.

## <a name="instructions"></a>Instrucciones

### <a name="step-1"></a>Paso 1:

Cree una subclave en **HKEY \_ classes \_ root** \\ *ProgID* \\ **Shell** \\ *CascadeMenuKey* y asigne a CascadeMenuKey un nombre como *CascadeTest*, por ejemplo. A continuación, agregue una entrada MUIVerb del tipo **reg \_ SZ** y asígnele un nombre como el menú de prueba en cascada 2, tal como se muestra en el siguiente ejemplo del registro.

```
HKEY_CLASSES_ROOT
   txtfile
      shell
         CascadeTest
            MUIVerb = Test Cascade Menu 2
```

### <a name="step-2"></a>Paso 2:

En la subclave *CascadeTest* que creó, agregue una subclave **ExtendedSubCommandsKey** y, a continuación, agregue los subcomandos de documento (de tipo **reg \_ SZ**); por ejemplo:

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Layout
               Properties
               Select all
```

Asegúrese de que el valor predeterminado de la subclave *Test Cascade Menu 2* esté vacío y se muestre como **(valor no establecido)**.

### <a name="step-3"></a>Paso 3:

Rellene los subverbos utilizando cualquiera de las siguientes implementaciones de verbo estático. Tenga en cuenta que la subclave CommandFlags representa los valores de EXPCMDFLAGS. Si desea agregar un separador antes o después del elemento de menú en cascada, use ECF \_ SEPARATORBEFORE (0x20) o ECF \_ SEPARATORAFTER (0x40). Para obtener una descripción de estas marcas de Windows 7 y versiones posteriores, vea [**IExplorerCommand:: GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags). ECF \_ SEPARATORBEFORE solo funciona para los elementos de menú de nivel superior. MUIVerb es de tipo **reg \_ SZ** y CommandFlags es de tipo **reg \_ DWORD**.

```
HKEY_CLASSES_ROOT
   txtile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Shell
                  cmd1
                     MUIVerb = Notepad
                     command
                        (Default) = %SystemRoot%\system32\notepad.exe %1
                  cmd2
                     MUIVerb = Wordpad
                     CommandFlags = 0x20
                     command
                        (Default) = C:\Program Files\Windows NT\Accessories\wordpad.exe %1
```

## <a name="remarks"></a>Observaciones

La siguiente captura de pantalla es una ilustración de los ejemplos anteriores de entradas de la clave del registro.

![captura de pantalla que muestra un ejemplo de un menú en cascada con opciones de Bloc de notas y WordPad](images/file-assoc/testcascademenu2.png)

 

 



