---
title: Implementar la página de propiedades de un complemento DSP
description: Implementar la página de propiedades de un complemento DSP
ms.assetid: 3dd3e547-fd06-4f01-8731-da1f8c958a32
keywords:
- Complementos de Windows Media Player, audio DSP
- complementos, DSP de audio
- Complementos de procesamiento de señal digital, propiedades de audio
- Complementos DSP, propiedades de audio
- Complementos DSP de audio, propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec87318b77fec4e9218398c1cb43dd5954a49e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903301"
---
# <a name="implementing-the-property-page-for-a-dsp-plug-in"></a>Implementar la página de propiedades de un complemento DSP

Windows Media Player puede mostrar una página de propiedades para cada complemento de DSP para permitir que los usuarios establezcan valores que cambian el comportamiento del complemento. Los usuarios pueden tener acceso a la página de propiedades desde **la pestaña** complementos del cuadro de diálogo Opciones; para ello, haga clic en el nombre del complemento DSP para seleccionarlo y, a continuación, haga clic en **propiedades**.

El código de ejemplo del Asistente para complementos de Windows Media Player proporciona una implementación predeterminada de una página de propiedades que incluye un solo cuadro de edición que recibe del usuario un valor que representa un factor de escala para el volumen de audio. Cuando el usuario hace clic en **aplicar**, la página de propiedades pasa este valor al objeto de complemento para que el complemento pueda cambiar el valor que usa para escalar el volumen durante el procesamiento.

## <a name="about-the-property-page-object"></a>Acerca del objeto de página de propiedades

El objeto de página de propiedades es un objeto COM que implementa la interfaz **IPropertyPage** . El código de ejemplo generado por el Asistente para complementos usa la implementación de ATL de **IPropertyPage**, que se documenta en la documentación de Visual C++ en MSDN. El código debe proporcionar al menos implementaciones de invalidación para **IPropertyPage:: OnInitDialog**, que controla el evento que se produce cuando se abre la página de propiedades y **IPropertyPage:: Apply**, que controla el evento que se produce cuando el usuario hace clic en **aplicar**. El Asistente para complementos genera código de ejemplo para cada uno de estos controladores de eventos. La implementación de ejemplo de **OnInitDialog** recupera un valor del registro para que pueda mostrar la configuración del factor de escala actual. La implementación de ejemplo de **Apply** valida los datos proporcionados por el usuario probando para asegurarse de que está dentro de un intervalo especificado y, a continuación, guarda el valor en el registro y, a continuación, pasa el valor (si es válido) al método put de la propiedad del complemento DSP, denominado **\_ Scale Scale**.

Además, tendrá que agregar código para controlar el evento que se produce cuando el usuario cambia un valor en un control que se proporciona en la página de propiedades. Por ejemplo, el Asistente para complementos implementa una función denominada **OnChangeScale**, que simplemente habilita el botón **aplicar** cuando el usuario cambia el texto en el cuadro de edición en la página de propiedades llamando al método **SetDirty** con un valor de argumento **true**.

## <a name="about-the-property-page-dialog-resource"></a>Acerca del recurso de cuadro de diálogo Página de propiedades

La interfaz de usuario de la página de propiedades se almacena como un recurso de cuadro de diálogo. Puede ver y editar fácilmente el cuadro de diálogo de la página de propiedades en Visual Studio; para ello, seleccione la pestaña **ResourceView** en la ventana del área de trabajo del proyecto, abra la carpeta del **cuadro de diálogo** y, a continuación, haga doble clic en el nombre del recurso de la página de propiedades. El editor de recursos de cuadro de diálogo de Visual Studio le proporciona las herramientas que necesita para agregar controles al cuadro de diálogo de la página de propiedades y para crear controladores de eventos que se asignan a los mensajes de Windows adecuados. Para obtener más información sobre cómo usar el editor de recursos en Visual Studio, consulte la ayuda de Visual Studio.

## <a name="about-ispecifypropertypages"></a>Acerca de ISpecifyPropertyPages

Si un complemento DSP proporciona una página de propiedades, el complemento debe implementar la interfaz **ISpecifyPropertyPages** . Esta interfaz contiene un solo método: **ISpecifyPropertyPages:: GetPages**. Este es el método que asocia la página de propiedades con el complemento DSP. Windows Media Player llama a este método cuando el usuario invoca la página de propiedades, pasando un parámetro de tipo CAUUID, que es una matriz contada de GUID. La implementación del complemento de ejemplo de **GetPages** rellena esta estructura con un único GUID que es el identificador de clase del objeto de página de propiedades del complemento. Windows Media Player usa el ID. de clase para crear el objeto de página de propiedades.

Es posible que observe que la implementación de ejemplo de **GetPages** usa **CoTaskMemAlloc** para asignar memoria para la estructura de GUID. Es responsabilidad del autor de la llamada, en este caso Windows Media Player, usar **CoTaskMemFree** para liberar la memoria. Para obtener más información sobre la estructura CAUUID, consulte la documentación del SDK de la plataforma.

## <a name="about-the-proxystub-dll"></a>Acerca de la DLL de proxy/código auxiliar

Para que un complemento de DSP funcione en Windows Media Player 11 que se ejecute en Windows Vista, debe proporcionar un archivo DLL de proxy/código auxiliar para las interfaces personalizadas utilizadas para comunicar los cambios de configuración desde un cuadro de diálogo de página de propiedades a la clase de complemento. Se deben calcular las referencias de las llamadas a métodos realizadas a través de estas interfaces cuando las llamadas se realizan a través de límites de proceso o apartamento. La versión más reciente del Asistente para complementos crea un proyecto de archivo DLL de código auxiliar/proxy de ejemplo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementar un complemento de DSP de audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




