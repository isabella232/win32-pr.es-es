---
description: En este tema se identifican varias estrategias de control de errores que se deben tener en cuenta al desarrollar componentes para COM+.
ms.assetid: 1ae5875b-8085-44f2-9071-c2a5d7543ac1
title: Estrategias para controlar errores en COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ca64546683fa45ac8df3bcb47534d8de482798
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361642"
---
# <a name="strategies-for-handling-errors-in-com"></a>Estrategias para controlar errores en COM+

En este tema se identifican varias estrategias de control de errores que se deben tener en cuenta al desarrollar componentes para COM+.

-   **Devuelve un valor HRESULT para todos los métodos de todas las interfaces de componente.**  COM+ usa **valores HRESULT** para informar sobre los errores al realizar llamadas de función o llamadas a métodos de interfaz. Un **HRESULT** indica si un método se ha producido correctamente o no e identifica la instalación asociada al error, como RPC, WIN32 o ITF para errores específicos de la interfaz. Además, las API del sistema proporcionan una búsqueda desde **un HRESULT** a una cadena que describe la condición de error. El uso de métodos **que devuelven valores HRESULT** es fundamental para los componentes bien escritos y son esenciales para el proceso de depuración. Microsoft Visual Basic define automáticamente cada método con **un HRESULT** como valor devuelto. En Microsoft Visual C++, debe devolver explícitamente **un HRESULT**. Para obtener información adicional sobre los HULT, vea [Estructura de códigos de error COM](/windows/desktop/com/structure-of-com-error-codes).
-   **Inicie el objeto de colección ErrorInfo por cualquier medio que la herramienta de desarrollo proporciona.** [**Los objetos de**](errorinfo.md) colección ErrorInfo a menudo se denominan excepciones COM porque permiten a un objeto pasar (o producir) información de error completa a su autor de la llamada, incluso a través de los límites de apartamento. El valor de este objeto de error genérico es que complementa un HRESULT, ampliando el tipo de información de error que puede devolver a un autor de la llamada. Cada **objeto de colección ErrorInfo** devuelve una descripción contextual, el origen del error y el identificador de interfaz del método que originó el error. También puede incluir punteros a una entrada en un archivo de ayuda. Automation proporciona tres interfaces para administrar el objeto de error. El componente debe implementar la **interfaz de automatización ISupportErrorInfo** para anunciar su compatibilidad con la **colección ErrorInfo.** Cuando se produce un error, el componente usa la interfaz de automatización **ICreateErrorInfo** para inicializar un objeto de error. Una vez que el autor de la llamada inspecciona el HRESULT y descubre que se produjo un error en la llamada al método, consulta el objeto para ver si admite la **colección ErrorInfo.** Si es así, el autor de la llamada usa la interfaz de automatización **IErrorInfo** para recuperar la información del error. Visual Basic programadores tienen acceso sencillo al objeto de colección **ErrorInfo,** que se expone a través del objeto Err. Puede generar errores con la función Err Raise y detectar errores con la **instrucción On Error.** La Visual Basic en tiempo de ejecución se encarga de la asignación. Si usa la compatibilidad con Visual C++ compilador COM, puede usar la clase de error com raise para notificar un error y la clase de error com para recuperar información \_ \_ de \_ \_ \_ error. COM+ no propagará las excepciones tradicionales de C++ como información **IErrorInfo** extendida. Para obtener información adicional sobre el **objeto de colección ErrorInfo,** vea "Control de errores" en la guía de Automation.
    > [!Note]  
    > COM requiere que todos los objetos de colección [**ErrorInfo**](errorinfo.md) se serializan por valor, lo que implica que los componentes que implementan la interfaz de automatización **IErrorInfo** también deben implementar y admitir la [**interfaz IMarshal.**](/windows/desktop/api/objidl/nn-objidl-imarshal) La **implementación de la interfaz IMarshal** debe admitir la serialización por valor para el componente.

     

-   **Use transacciones para administrar errores de recursos compartidos.** Las transacciones automáticas pueden reducir significativamente la cantidad de código de control de errores que debe escribir al usar administradores de recursos administrados por estado. Sin embargo, las transacciones no eliminan por completo la necesidad de control de errores. Sigue siendo necesario devolver códigos de error de los métodos de interfaz y comprobar esos códigos de error dentro del autor de la llamada para evitar realizar un trabajo innecesario para una transacción desfasada. Para obtener información adicional sobre cómo combinar el control de errores con el procesamiento de transacciones, vea Acelerar transacciones [notificando al objeto raíz](speeding-transactions-by-notifying-the-root-object.md).
-   **Generar errores explícitamente.** Evite dejar que la información de error deje un objeto a menos que el objeto genera explícitamente el error. Detectar todos los errores generados por la herramienta y controlarlos en el código del componente. Como mínimo, incluya un controlador estándar para notificar errores inesperados de una manera coherente.
-   **Use el intervalo de \_ errores FACILITY ITF para notificar errores específicos de la interfaz.** Los errores específicos de la interfaz deben estar en el intervalo de errores \_ de FACILITY ITF, entre 0x0200 y 0xFFFF. Puede definir un código de error personalizado en Visual Basic como un desplazamiento de vbObjectError. Use la macro MAKE HRESULT en C++ para introducir un código de error específico \_ de la interfaz, como se muestra en el ejemplo siguiente:

    ``` syntax
    const HRESULT ERROR_NUMBER = MAKE_HRESULT (SEVERITY_ERROR, FACILITY_ITF, 10);
    ```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aislamiento de errores y directiva de conmutación por error](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Buscar el origen de un error](finding-the-source-of-an-error.md)
</dt> <dt>

[Cómo modifica COM+ los valores devueltos](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretación de códigos de error](interpreting-error-codes.md)
</dt> <dt>

[Solución de problemas](troubleshooting.md)
</dt> </dl>

 

 
