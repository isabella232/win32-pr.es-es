---
title: Implementar la página de propiedades para un complemento DSP
description: Implementar la página de propiedades para un complemento DSP
ms.assetid: 3dd3e547-fd06-4f01-8731-da1f8c958a32
keywords:
- Reproductor de Windows Media complementos,DSP de audio
- complementos, DSP de audio
- complementos de procesamiento de señal digital, propiedades de audio
- Complementos de DSP, propiedades de audio
- complementos de DSP de audio, propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec87318b77fec4e9218398c1cb43dd5954a49e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249626"
---
# <a name="implementing-the-property-page-for-a-dsp-plug-in"></a>Implementar la página de propiedades para un complemento DSP

Reproductor de Windows Media puede mostrar una página de propiedades para cada complemento de DSP para permitir a los usuarios establecer valores que cambien el comportamiento del complemento. Los usuarios pueden acceder  a la página de propiedades desde la pestaña Complementos del cuadro de diálogo Opciones haciendo clic en el nombre del complemento DSP para seleccionarlo y, a continuación, haciendo clic en **Propiedades.**

El código de ejemplo del Asistente para complementos de Reproductor de Windows Media proporciona una implementación predeterminada de una página de propiedades que incluye un único cuadro de edición que recibe del usuario un valor que representa un factor de escala para el volumen de audio. Cuando el usuario hace clic en **Aplicar**, la página de propiedades pasa este valor al objeto de complemento para que el complemento pueda cambiar el valor que usa para escalar el volumen durante el procesamiento.

## <a name="about-the-property-page-object"></a>Acerca del objeto de página de propiedades

El objeto de página de propiedades es un objeto COM que implementa la **interfaz IPropertyPage.** El código de ejemplo generado por el asistente para complementos usa la implementación ATL de **IPropertyPage**, que se documenta en la documentación de Visual C++ en MSDN. El código debe proporcionar al menos implementaciones de invalidación para **IPropertyPage::OnInitDialog**, que controla el evento que se produce cuando se abre la página de propiedades, e **IPropertyPage::Apply**, que controla el evento que se produce cuando el usuario hace clic en **Aplicar**. El asistente para complementos genera código de ejemplo para cada uno de estos controladores de eventos. La implementación de ejemplo **de OnInitDialog** recupera un valor del Registro para que pueda mostrar la configuración del factor de escala actual. La implementación de ejemplo de **Apply** valida la entrada del usuario mediante pruebas para asegurarse de que se encuentra dentro de un intervalo especificado, luego conserva el valor en el registro y, a continuación, pasa el valor (si es válido) al método put de la propiedad del complemento DSP, denominado **put \_ scale.**

Además, deberá agregar código para controlar el evento que se produce cuando el usuario cambia un valor en un control que proporcione en la página de propiedades. Por ejemplo, el asistente para complementos implementa una función denominada  **OnChangeScale**, que simplemente habilita el botón Aplicar cuando el usuario cambia el texto del cuadro de edición de la página de propiedades mediante una llamada al método **SetDirty** con un valor de argumento **TRUE.**

## <a name="about-the-property-page-dialog-resource"></a>Acerca del recurso de cuadro de diálogo de la página de propiedades

La interfaz de usuario de la página de propiedades se almacena como un recurso de diálogo. Para ver y editar fácilmente el cuadro de diálogo de la página de propiedades en Visual Studio,  seleccione la pestaña **ResourceView** en la ventana Área de trabajo de Project, abra la carpeta Diálogo y, a continuación, haga doble clic en el nombre del recurso de la página de propiedades. El editor de recursos de diálogo de Visual Studio proporciona las herramientas necesarias para agregar controles al cuadro de diálogo de página de propiedades y para crear controladores de eventos que se asignan a los mensajes Windows adecuados. Para obtener más información sobre cómo usar el editor de recursos en Visual Studio, consulte Visual Studio Ayuda.

## <a name="about-ispecifypropertypages"></a>Acerca de ISpecifyPropertyPages

Si un complemento DSP proporciona una página de propiedades, el complemento debe implementar la **interfaz ISpecifyPropertyPages.** Esta interfaz solo contiene un método: **ISpecifyPropertyPages::GetPages**. Este es el método que asocia la página de propiedades con el complemento DSP. Reproductor de Windows Media llama a este método cuando el usuario invoca la página de propiedades, pasando un parámetro de tipo CAUUID, que es una matriz con recuento de GUID. La implementación de complemento de ejemplo de **GetPages** rellena esta estructura con un único GUID que es el identificador de clase del objeto de página de propiedades del complemento. Reproductor de Windows Media utiliza el identificador de clase para crear el objeto de página de propiedades.

Es posible que observe que la implementación de ejemplo de **GetPages** usa **CoTaskMemAlloc para** asignar memoria para la estructura GUID. Es responsabilidad del autor de la llamada, en este Reproductor de Windows Media, usar **CoTaskMemFree** para liberar la memoria. Para más información sobre la estructura CAUUID, consulte la documentación del SDK de plataforma.

## <a name="about-the-proxystub-dll"></a>Acerca del archivo DLL de proxy o código auxiliar

Para que un complemento DSP funcione en Reproductor de Windows Media 11 que se ejecuta en Windows Vista, debe proporcionar un archivo DLL de proxy o código auxiliar para las interfaces personalizadas que se usan para comunicar los cambios en la configuración de un cuadro de diálogo de página de propiedades a la clase de complemento. Las llamadas de método realizadas a través de estas interfaces se deben serializar cuando las llamadas se realizan a través de los límites de proceso o apartamento. La versión más reciente del asistente para complementos crea un proyecto dll de proxy o de código auxiliar de ejemplo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de un complemento dsp de audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




