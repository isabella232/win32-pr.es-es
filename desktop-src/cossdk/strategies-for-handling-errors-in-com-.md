---
description: En este tema se identifican varias estrategias de control de errores que se deben tener en cuenta al desarrollar componentes para COM+.
ms.assetid: 1ae5875b-8085-44f2-9071-c2a5d7543ac1
title: Estrategias para controlar errores en COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ca64546683fa45ac8df3bcb47534d8de482798
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696110"
---
# <a name="strategies-for-handling-errors-in-com"></a>Estrategias para controlar errores en COM+

En este tema se identifican varias estrategias de control de errores que se deben tener en cuenta al desarrollar componentes para COM+.

-   **Devuelve un valor HRESULT para todos los métodos de todas las interfaces de componentes.**  COM+ usa valores **HRESULT** para informar de los errores que se produzcan al realizar llamadas a funciones o llamadas a métodos de interfaz. Un **valor HRESULT** indica si un método tuvo éxito o no, e identifica la instalación asociada al error, como RPC, Win32 o ITF para los errores específicos de la interfaz. Además, las API del sistema proporcionan una búsqueda de un **valor HRESULT** a una cadena que describe la condición de error. El uso de métodos que devuelven valores **HRESULT** es fundamental para los componentes bien escritos y son esenciales para el proceso de depuración. Microsoft Visual Basic define automáticamente cada método con un **HRESULT** como un valor devuelto. En Microsoft Visual C++, debe devolver explícitamente un **valor HRESULT**. Para obtener información adicional sobre los valores HRESULT, vea [estructura de los códigos de error com](/windows/desktop/com/structure-of-com-error-codes).
-   **Inicie el objeto de colección ErrorInfo por cualquier medio que proporcione la herramienta de desarrollo.** Los objetos de colección [**errorInfo**](errorinfo.md) se suelen denominar excepciones com porque permiten que un objeto pase (o produzca) información de error enriquecida a su llamador, incluso a través de límites de apartamento. El valor de este objeto de error genérico es que complementa un HRESULT y extiende el tipo de información de error que se puede devolver a un llamador. Cada objeto de colección **errorInfo** devuelve una descripción contextual, el origen del error y el identificador de interfaz del método que originó el error. También puede incluir punteros a una entrada en un archivo de ayuda. Automation proporciona tres interfaces para administrar el objeto de error. El componente debe implementar la interfaz de automatización de **ISupportErrorInfo** para anunciar su compatibilidad con la colección **errorInfo** . Cuando se produce un error, el componente usa la interfaz de automatización **ICreateErrorInfo** para inicializar un objeto de error. Una vez que el llamador inspecciona el valor HRESULT y detecta que se produjo un error en la llamada al método, consulta el objeto para ver si es compatible con la colección **errorInfo** . Si lo hace, el llamador utiliza la interfaz de automatización de **IErrorInfo** para recuperar la información de error. Visual Basic los programadores tienen acceso sencillo al objeto de colección **errorInfo** , que se expone a través del objeto Err. Puede generar errores con la función raise raise y detectar errores con la instrucción **on error** . La Visual Basic capa en tiempo de ejecución se encarga de la asignación. Si usa la compatibilidad con el compilador COM Visual C++, puede utilizar \_ la \_ clase de error de generación com \_ para notificar un error y la \_ clase de \_ error com para recuperar la información de error. COM+ no propagará las excepciones de C++ tradicionales como información extendida de **IErrorInfo** . Para obtener más información sobre el objeto de colección **errorInfo** , vea el tema sobre el control de errores en la guía de automatización.
    > [!Note]  
    > COM requiere que todos los objetos de colección [**errorInfo**](errorinfo.md) calculen las referencias por valor, lo que implica que los componentes que implementan la interfaz de automatización **IErrorInfo** también deben implementar y admitir la interfaz [**IMarshal**](/windows/desktop/api/objidl/nn-objidl-imarshal) . La implementación de la interfaz **IMarshal** debe admitir la serialización por valor para el componente.

     

-   **Usar transacciones para administrar errores de recursos compartidos.** Las transacciones automáticas pueden reducir de forma significativa la cantidad de código de control de errores que se debe escribir al usar administradores de recursos administrados por el estado. Sin embargo, las transacciones no eliminan por completo la necesidad de control de errores. Todavía tiene que devolver códigos de error de los métodos de interfaz y comprobar los códigos de error dentro del llamador para evitar realizar un trabajo innecesario para una transacción desactivada. Para obtener información adicional sobre cómo combinar el control de errores con el procesamiento de transacciones, consulte [acelerar las transacciones notificando el objeto raíz](speeding-transactions-by-notifying-the-root-object.md).
-   **Generar errores explícitamente.** Evite permitir que la información de error deje un objeto a menos que el objeto genere explícitamente el error. Detectar todos los errores generados por la herramienta y controlarlos en el código de componente. Como mínimo, incluya un controlador estándar para informar de errores inesperados de una manera coherente.
-   **Use el \_ intervalo de errores de instalación ITF para informar de errores específicos de la interfaz.** Los errores específicos de la interfaz deben estar en el \_ intervalo de errores de instalación ITF, entre 0x0200 y 0xFFFF. Puede definir un código de error personalizado en Visual Basic como un desplazamiento desde vbObjectError. Use la \_ macro make HRESULT en C++ para introducir un código de error específico de la interfaz, tal como se muestra en el ejemplo siguiente:

    ``` syntax
    const HRESULT ERROR_NUMBER = MAKE_HRESULT (SEVERITY_ERROR, FACILITY_ITF, 10);
    ```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aislamiento de errores y Directiva FailFast](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Buscar el origen de un error](finding-the-source-of-an-error.md)
</dt> <dt>

[Cómo modifica COM+ los valores devueltos](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretar códigos de error](interpreting-error-codes.md)
</dt> <dt>

[Solución de problemas](troubleshooting.md)
</dt> </dl>

 

 
