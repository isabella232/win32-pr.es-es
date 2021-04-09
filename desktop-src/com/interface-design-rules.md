---
title: Reglas de diseño de interfaz
description: En esta sección se proporciona un breve resumen de las reglas y las instrucciones de diseño de la interfaz.
ms.assetid: c43fc385-bcd6-45fc-91b2-ad9827fdb15c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c1cde73527ac79a2e4442910e3053ed96748337
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149645"
---
# <a name="interface-design-rules"></a>Reglas de diseño de interfaz

En esta sección se proporciona un breve resumen de las reglas y las instrucciones de diseño de la interfaz. Algunas de estas reglas son específicas de la arquitectura COM, mientras que otras son restricciones impuestas por el lenguaje de diseño de la interfaz, MIDL. Para obtener información detallada sobre el diseño de la interfaz COM, vea [anatomía de un archivo IDL](anatomy-of-an-idl-file.md).

Por definición, un objeto no es un objeto COM a menos que implemente la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) o una interfaz que se deriva de **IUnknown**. Además, las siguientes reglas se aplican a todas las interfaces implementadas en un objeto COM:

-   Deben tener un identificador de interfaz único (IID).
-   Deben ser inmutables. Una vez que se crean y publican, ninguna parte de la definición puede cambiar.
-   Todos los métodos de interfaz deben devolver un valor **HRESULT** para que las partes del sistema que controlan el procesamiento remoto puedan notificar errores de RPC.
-   Todos los parámetros de cadena de los métodos de interfaz deben ser Unicode.
-   Los tipos de datos deben ser remotos. Si no puede convertir un tipo de datos en un tipo utilizable de forma remota, tendrá que crear sus propias rutinas de serialización y desserialización. También, **LPVOID** o **void \***, no tiene ningún significado en un equipo remoto. Use un puntero a [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), si es necesario.

> [!Note]  
> La implementación actual de MIDL no controla la sobrecarga de funciones o la herencia múltiple.

 

## <a name="other-interface-design-considerations"></a>Otras consideraciones de diseño de la interfaz

Use punteros a datos con sumo cuidado. Para volver a crear los datos en el espacio de direcciones del proceso al que se llama, el tiempo de ejecución de RPC debe conocer el tamaño exacto de los datos. Si, por ejemplo, un **parámetro \* Char** apunta a un búfer de caracteres en lugar de a un solo carácter, no se pueden volver a crear correctamente los datos. Use la sintaxis disponible con MIDL para describir con precisión las estructuras de datos representadas por las definiciones de tipo.

La inicialización es esencial para los punteros que se incrustan en matrices y estructuras y se pasan a través de los límites del proceso. Los punteros no inicializados pueden funcionar cuando se pasan a un programa en el mismo espacio de proceso, pero los servidores proxy y los códigos auxiliares suponen que todos los punteros se inicializan con direcciones válidas o son NULL.

Tenga cuidado al aplicar alias a los punteros (permitiendo que los punteros señalen a la misma parte de la memoria). Si el alias es intencionado, estos punteros se deben declarar con alias en el archivo IDL. Los punteros declarados como sin alias no deben tener el alias nunca.

Preste atención a la asignación y liberación de memoria. Recuerde que, a menos que indique explícitamente que un objeto COM (mediante el atributo [**allocate**](/windows/desktop/Midl/allocate) ) no libere una estructura de datos que se creó durante una llamada fuera de proceso, esa estructura se destruirá cuando se complete la llamada. Además, tenga en cuenta la sobrecarga potencialmente destructiva creada por una asignación ineficaz de estructuras de datos en las que se deben calcular las referencias y cuyas referencias no se han calculado.

Por último, tenga cuidado al definir los valores devueltos **HRESULT** para no crear códigos de error que entren en conflicto con los códigos ITF de la instalación definida por com \_ (los valores entre 0x0000 y 0x01FF están reservados) o que entren en conflicto con otros valores **HRESULT** con el mismo valor. Siempre que sea posible, use los valores devueltos de correcto y error de COM universal y use un parámetro de [**salida**](/windows/desktop/Midl/out-idl) , en lugar de un **valor HRESULT**, para devolver información específica de la llamada de función.

Para obtener más información, vea los temas siguientes:

-   [Diseño de interfaces remotas](designing-remotable-interfaces.md)
-   [Usar una interfaz COM](using-a-com-interface.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Definiciones de interfaz y bibliotecas de tipos](/windows/desktop/Midl/interface-definitions-and-type-libraries)
</dt> </dl>

 

 