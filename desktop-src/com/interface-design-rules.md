---
title: Reglas de diseño de interfaz
description: En esta sección se proporciona un breve resumen de las reglas y las directrices de diseño de la interfaz.
ms.assetid: c43fc385-bcd6-45fc-91b2-ad9827fdb15c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c1cde73527ac79a2e4442910e3053ed96748337
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060902"
---
# <a name="interface-design-rules"></a>Reglas de diseño de interfaz

En esta sección se proporciona un breve resumen de las reglas y las directrices de diseño de la interfaz. Algunas de estas reglas son específicas de la arquitectura COM, mientras que otras son restricciones impuestas por el lenguaje de diseño de interfaz, MIDL. Para obtener más información sobre el diseño de la interfaz COM, vea [Anatomía de un archivo IDL](anatomy-of-an-idl-file.md).

Por definición, un objeto no es un objeto COM a menos que implemente la [**interfaz IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) o una interfaz derivada de **IUnknown**. Además, las reglas siguientes se aplican a todas las interfaces implementadas en un objeto COM:

-   Deben tener un identificador de interfaz único (IID).
-   Deben ser inmutables. Una vez creados y publicados, no puede cambiar ninguna parte de su definición.
-   Todos los métodos de interfaz deben devolver **un valor HRESULT** para que las partes del sistema que controlan el procesamiento remoto puedan notificar errores RPC.
-   Todos los parámetros de cadena de los métodos de interfaz deben ser Unicode.
-   Los tipos de datos deben ser remotables. Si no puede convertir un tipo de datos en un tipo remotable, tendrá que crear sus propias rutinas de serialización y desmarque. Además, **LPVOID** o **\* void* _, no tiene ningún significado en un equipo remoto. Use un puntero a [_ *IUnknown* *](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), si es necesario.

> [!Note]  
> La implementación actual de MIDL no controla la sobrecarga de funciones ni la herencia múltiple.

 

## <a name="other-interface-design-considerations"></a>Otras consideraciones de diseño de interfaz

Use punteros a los datos con mucho cuidado. Para volver a crear los datos en el espacio de direcciones del proceso al que se llama, el tiempo de ejecución rpc debe conocer el tamaño exacto de los datos. Por ejemplo, si un parámetro **CHAR \*** apunta a un búfer de caracteres en lugar de a un solo carácter, los datos no se pueden volver a crear correctamente. Use la sintaxis disponible con MIDL para describir con precisión las estructuras de datos representadas por las definiciones de tipo.

La inicialización es esencial para los punteros que se incrustan en matrices y estructuras y se pasan a través de los límites del proceso. Los punteros sin inicializar pueden funcionar cuando se pasan a un programa en el mismo espacio de proceso, pero los servidores proxy y los códigos auxiliares asumen que todos los punteros se inicializan con direcciones válidas o son null.

Tenga cuidado al crear un alias de punteros (lo que permite que los punteros apunten al mismo fragmento de memoria). Si el alias es intencionado, estos punteros deben declararse con alias en el archivo IDL. Los punteros declarados como no con contorno nunca se deben alias entre sí.

Preste atención a cómo asignar y liberar memoria. Recuerde que, a menos que indique explícitamente a un objeto COM (mediante el atributo [**allocate)**](/windows/desktop/Midl/allocate) que no liberara una estructura de datos que se creó durante una llamada fuera de proceso, esa estructura se destruirá cuando se complete la llamada. Además, tenga en cuenta la sobrecarga potencialmente destructiva creada por la asignación ineficaz de estructuras de datos que ahora se deben serializar y desmarmar.

Por último, tenga cuidado al definir los valores devueltos **de HRESULT** para que no cree códigos de error que entren en conflicto con los códigos ITF FACILITY definidos por COM (los valores entre 0x0000 y 0x01FF están reservados) o que entren en conflicto con otros \_ valores **HRESULT** con el mismo valor. Siempre que sea posible, use los valores devueltos com correctos y de error universales y use un parámetro [**out,**](/windows/desktop/Midl/out-idl) en lugar de **un valor HRESULT,** para devolver información específica de la llamada de función.

Para obtener más información, vea los temas siguientes:

-   [Diseño de interfaces remotas](designing-remotable-interfaces.md)
-   [Uso de una interfaz COM](using-a-com-interface.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Definiciones de interfaz y bibliotecas de tipos](/windows/desktop/Midl/interface-definitions-and-type-libraries)
</dt> </dl>

 

 