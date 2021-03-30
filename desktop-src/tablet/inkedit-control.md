---
description: El control InkEdit proporciona una manera fácil de capturar, reconocer y mostrar la entrada de lápiz.
ms.assetid: a1dfa254-cade-44c5-8fdd-74bb40849063
title: Control InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6d5441506ee791eefddba05b9b1f3ddb8a8ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910757"
---
# <a name="inkedit-control"></a>Control InkEdit

El control [InkEdit](inkedit-control-reference.md) proporciona una manera fácil de capturar, reconocer y mostrar la entrada de lápiz.

Esta implementación del control [InkEdit](inkedit-control-reference.md) se basa en el control [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) . La implementación administrada (.NET Framework) de [InkEdit](/previous-versions/ms835842(v=msdn.10)) se basa en el control [**RichTextBox**](/previous-versions/windows/) .

El propósito principal del control [InkEdit](inkedit-control-reference.md) es recopilar la tinta, reconocerla y mostrarla en forma de texto. Además, permite mostrar la entrada de lápiz como un objeto incrustado con capacidades de formato de texto, como negrita y subrayado.

## <a name="gestures-and-correction"></a>Gestos y corrección

[InkEdit](inkedit-control-reference.md) admite los siguientes gestos.



| Gesto                                                                    | Nombre del gesto              | Acción               |
|----------------------------------------------------------------------------|---------------------------|----------------------|
| ![gesto de abajo a la izquierda](images/d8b00c0a-f450-4f71-980f-3bca1b558e4c.gif)      | Inferior izquierda<br/>      | Entrar<br/>     |
| ![gesto hacia abajo-izquierda-largo](images/b8cb23b5-b947-477d-922f-2ffb42756804.gif) | Abajo-izquierda-largo<br/> | Entrar<br/>     |
| ![gesto de arriba a la derecha](images/02c34d24-c2d7-404f-b99a-742ba6de7f0c.gif)       | Arriba a la derecha<br/>       | Pestaña<br/>       |
| ![gesto de arriba a la derecha.](images/5e3522d3-2920-4a86-86ae-f29b01d93993.gif) | Arriba-a la derecha<br/>  | Pestaña<br/>       |
| ![gesto derecho](images/864cf4e1-2619-49cf-ac96-72994232e465.jpg)          | Right<br/>          | Space<br/>     |
| ![gesto izquierdo](images/ce60cc20-1769-428d-80de-7f47c86021fb.jpg)           | Left<br/>           | Retroceso<br/> |



 

Los eventos de gestos que puede controlar contienen información de movimiento, trazo y cursor que puede usar para enviar texto a [InkEdit](inkedit-control-reference.md) o colocar datos en el portapapeles.

[InkEdit](inkedit-control-reference.md) también proporciona una interfaz de usuario de corrección que permite a los usuarios ver y seleccionar alternativas, usar el teclado en pantalla y reconocedores de caracteres, letras y bloques.

## <a name="other-details"></a>Otros detalles

[InkEdit](inkedit-control-reference.md) está diseñado para funcionar bien en un escenario de formulario para una sola línea, así como para la entrada y edición de texto de varias líneas. El uso previsto principal de InkEdit es obtener la entrada de texto de un usuario en forma de escritura a mano. De forma predeterminada, se reconoce la entrada manuscrita y el texto se inserta en su lugar. La interfaz de usuario predeterminada para InkEdit es similar a la del control [**RichTextBox**](/previous-versions/windows/) , excepto cuando el usuario está poniendo la tinta. Puede mostrar la entrada de lápiz original en lugar de texto; sin embargo, la tinta se escala hasta el tamaño de la fuente de entrada actual del control InkEdit y se muestra en línea con otro texto.

> [!Note]  
> Por motivos de seguridad, debe utilizar los procedimientos estándar para abrir o cerrar un archivo, transmitir la entrada/salida y establecer la propiedad [**RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) o [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) .

 

El control [InkEdit](inkedit-control-reference.md) se establece para que reconozca la entrada de lápiz como texto de forma predeterminada. Para permitir que los usuarios agreguen tinta como tinta, establezca la propiedad [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) en **InsertAsInk**.

Para obtener información de referencia detallada sobre el control [InkEdit](inkedit-control-reference.md) , vea InkEdit.

> [!Note]  
> Si usa el control Win32 [InkEdit](inkedit-control-reference.md) y lo coloca dentro de un cuadro de grupo, asegúrese de que el cuadro tiene un estilo transparente. de lo contrario, InkEdit no puede recopilar entradas manuscritas.

 

> [!Note]  
> Para asegurarse de que la tinta se muestra correctamente, llame al método de [**actualización**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh) del control [InkEdit](inkedit-control-reference.md) cuando reciba un evento [**HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1) o [**VScroll**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1) .

 

En las secciones siguientes se detalla el uso del control [InkEdit](inkedit-control-reference.md) :

-   [Crear instancias de InkEdit](instantiating-inkedit.md)
-   [Diferencias entre Word y el reconocimiento de caracteres](word-vs--character-recognition.md)
-   [Mostrar la entrada de lápiz como entrada de lápiz](displaying-ink-as-ink.md)
-   [Usar InkEdit en versiones anteriores de Windows](using-inkedit-on-earlier-versions-of-windows.md)
-   [Uso de un diccionario de aplicación con InkEdit](using-an-application-dictionary-with-inkedit.md)

 

