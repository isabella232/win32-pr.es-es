---
description: Explica cómo crear un control de entrada matemática.
ms.assetid: 59976b01-9032-4226-a160-e9b2d4b8b23b
title: Creación de un Control de entrada matemática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5084f29943395bc6781fe20598f86bdc08c6c61
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360329"
---
# <a name="creating-a-math-input-control"></a>Creación de un Control de entrada matemática

Para crear el control de entrada matemática, debe:

-   [Incluir encabezados y bibliotecas para el Control de entrada matemática](#include-headers-and-libraries-for-the-math-input-control)
-   [Declarar el puntero de control y llamar a CoInitialize en el puntero de control](#declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer)
-   [Mostrar el control](#show-the-control)

## <a name="include-headers-and-libraries-for-the-math-input-control"></a>Incluir encabezados y bibliotecas para el Control de entrada matemática

El código siguiente debe colocarse en la parte superior del código, donde se va a usar el control de entrada matemática.


```
   // includes for implementation
   #include "micaut.h"
   #include "micaut_i.c"
   
```



Este código agregará compatibilidad con el control de entrada matemática a la aplicación.

## <a name="declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer"></a>Declarar el puntero de control y llamar a CoInitialize en el puntero de control

Después de incluir los encabezados del control, puede declarar el puntero de control y llamar a CoInitialize en él para crear un identificador para la interfaz de control de entrada matemática. El código siguiente se puede colocar en una clase o como una variable global en la implementación de la aplicación:


```
   CComPtr<IMathInputControl> g_spMIC; // Math Input Control
   
```



El código siguiente muestra cómo puede llamar a CoInitialize en el puntero de control.


```
   HRESULT hr = CoInitialize(NULL);
   hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
   
```



Después de llamar a CoInitialize en el puntero de control, tiene una referencia al control y puede acceder a los métodos del control. Por ejemplo, podría habilitar el conjunto extendido de controles como se muestra en el ejemplo siguiente.


```
   hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
   
```



## <a name="show-the-control"></a>Mostrar el control

El control no aparecerá automáticamente después de crearlo. Para mostrar el control, llame al [**método Show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) en la referencia de control que creó en el paso anterior. El código siguiente muestra cómo [**se**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) puede llamar al método Show.


```
   hr = g_spMIC->Show();
   
```



Una vez que se muestre el control, tendrá un aspecto parecido al de la ilustración siguiente.

![captura de pantalla que muestra el control de entrada matemática](images/mic.png)

Tenga en cuenta que he habilitado el conjunto extendido de botones para que **Rehacer** y **Deshacer** estén disponibles.

 

 
