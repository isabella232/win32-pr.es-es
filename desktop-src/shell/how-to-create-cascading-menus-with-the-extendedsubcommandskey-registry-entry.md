---
description: En Windows 7 y versiones posteriores, puede usar la subclave ExtendedSubCommandsKey para crear menús en cascada extendidos.
ms.assetid: 6E8B4FB7-D4DB-4DBC-AF6F-59D02CB6AB13
title: Crear menús en cascada con la entrada del Registro ExtendedSubCommandsKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220a38825ae250a0d58d30bc7de93f290f819eb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361058"
---
# <a name="how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a>Cómo crear menús en cascada con la entrada del Registro ExtendedSubCommandsKey

En Windows 7 y versiones posteriores, puede usar la subclave **ExtendedSubCommandsKey** para crear menús en cascada extendidos.

La siguiente captura de pantalla es un ejemplo de un menú en cascada extendido.

![captura de pantalla que muestra el menú en cascada extendido para dispositivos](images/file-assoc/extendedsubcommandskey.png)

Dado **que HKEY \_ CLASSES \_ ROOT** es una combinación de **HKEY CURRENT \_ \_ USER** y **HKEY LOCAL \_ \_ MACHINE,** puede registrar los subverberos en la subclave clases de software **HKEY CURRENT \_ \_ USER.** \\  \\  La ventaja de hacerlo es que no se requiere permiso elevado. Otras asociaciones de archivo pueden reutilizar todo este conjunto de verbos especificando la misma subclave **ExtendedSubCommandsKey.** Si no necesita volver a usar este conjunto de verbos, puede enumerar los verbos bajo el elemento primario. En este caso, asegúrese de que el valor predeterminado del elemento primario está vacío, como se muestra en el ejemplo de entrada del Registro de esta sección.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Paso 1:

Cree una subclave en el shell CascadeMenuKey de **HKEY \_ CLASSES \_ ROOT** ProgID y asigne a CascadeMenuKey un nombre como \\  \\  \\  *CascadeTest,* por ejemplo. A continuación, agregue una entrada DE LAVERB de **tipo REG \_ SZ** y asímble un nombre como Test Cascade Menu 2 (Menú en cascada de prueba 2), como se muestra en el siguiente ejemplo del Registro.

```
HKEY_CLASSES_ROOT
   txtfile
      shell
         CascadeTest
            MUIVerb = Test Cascade Menu 2
```

### <a name="step-2"></a>Paso 2:

En la subclave *CascadeTest* que ha creado, agregue una subclave **ExtendedSubCommandsKey** y, a continuación, agregue los subcomandos del documento (de tipo **REG \_ SZ**); por ejemplo:

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

Asegúrese de que el valor predeterminado de la subclave *Test Cascade Menu 2* está vacío y se muestra **como (valor no establecido).**

### <a name="step-3"></a>Paso 3:

Rellene los subverberos mediante cualquiera de las siguientes implementaciones de verbo estático. Tenga en cuenta que la subclave CommandFlags representa valores EXPCMDFLAGS. Si desea agregar un separador antes o después del elemento de menú en cascada, use ECF \_ SEPARATORBEFORE (0x20) o ECF \_ SEPARATORAFTER (0x40). Para obtener una descripción de estas Windows 7 y posteriores, vea [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags). ECF \_ SEPARATORBEFORE solo funciona para los elementos de menú de nivel superior. MUIVerb es de tipo **REG \_ SZ** y CommandFlags es de tipo **REG \_ DWORD.**

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

La siguiente captura de pantalla es una ilustración de los ejemplos de entrada de clave del Registro anteriores.

![captura de pantalla que muestra un ejemplo de un menú en cascada que muestra las opciones del Bloc de notas y el Bloc de palabras](images/file-assoc/testcascademenu2.png)

 

 



