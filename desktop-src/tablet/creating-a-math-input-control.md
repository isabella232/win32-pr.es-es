---
description: Explica cómo crear un control de entrada matemática.
ms.assetid: 59976b01-9032-4226-a160-e9b2d4b8b23b
title: Crear un control de entrada matemática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5084f29943395bc6781fe20598f86bdc08c6c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553304"
---
# <a name="creating-a-math-input-control"></a>Crear un control de entrada matemática

Para crear el control de entrada matemática, debe:

-   [Incluir encabezados y bibliotecas para el control de entrada matemática](#include-headers-and-libraries-for-the-math-input-control)
-   [Declare el puntero de control y llame a CoInitialize en el puntero de control](#declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer)
-   [Mostrar el control](#show-the-control)

## <a name="include-headers-and-libraries-for-the-math-input-control"></a>Incluir encabezados y bibliotecas para el control de entrada matemática

El código siguiente debe colocarse en la parte superior del código donde se va a usar el control de entrada matemática.


```
   // includes for implementation
   #include "micaut.h"
   #include "micaut_i.c"
   
```



Este código agregará compatibilidad para el control de entrada matemática a la aplicación.

## <a name="declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer"></a>Declare el puntero de control y llame a CoInitialize en el puntero de control

Una vez incluidos los encabezados para el control, puede declarar el puntero de control y puede llamar a CoInitialize en él para crear un identificador de la interfaz de control de entrada matemática. El siguiente código se puede colocar en una clase o como una variable global en la implementación de la aplicación:


```
   CComPtr<IMathInputControl> g_spMIC; // Math Input Control
   
```



En el código siguiente se muestra cómo se puede llamar a CoInitialize en el puntero de control.


```
   HRESULT hr = CoInitialize(NULL);
   hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
   
```



Después de llamar a CoInitialize en el puntero de control, tiene una referencia al control y puede tener acceso a los métodos del control. Por ejemplo, podría habilitar el conjunto extendido de controles tal como se muestra en el ejemplo siguiente.


```
   hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
   
```



## <a name="show-the-control"></a>Mostrar el control

El control no aparecerá automáticamente después de crearlo. Para mostrar el control, llame al método [**Show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) en la referencia de control que creó en el paso anterior. En el código siguiente se muestra cómo se puede llamar al método [**Show**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) .


```
   hr = g_spMIC->Show();
   
```



Una vez que se muestre el control, tendrá un aspecto similar al de la siguiente ilustración.

![captura de pantalla que muestra el control de entrada matemática](images/mic.png)

Tenga en cuenta que he habilitado el conjunto extendido de botones para que las operaciones de **rehacer** y **Deshacer** estén disponibles.

 

 
