---
description: El propósito del contenedor del proveedor es encapsular y usar las interfaces COM de bajo nivel (proporcionadas por los fabricantes de tarjetas inteligentes) para una tarjeta inteligente determinada. Microsoft no proporciona estas interfaces.
ms.assetid: 7bc26f7b-c355-448a-9f23-4ccfffea2fef
title: Proveedor de servicios de contenedor de proveedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b7d22fea8e450111e1611f2ec069697c229a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154140"
---
# <a name="vendor-wrapper-service-provider"></a>Proveedor de servicios de contenedor de proveedores

El propósito del contenedor del proveedor es encapsular y usar las interfaces COM de bajo nivel (proporcionadas por los fabricantes de tarjetas inteligentes) para una tarjeta inteligente determinada. Microsoft no proporciona estas interfaces.

![contenedor de proveedores](images/scspart1.png)

Tal como se describe en la parte 6 de la *especificación de interoperabilidad para ICCS y los sistemas informáticos personales* (consulte las especificaciones en [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ), la funcionalidad expuesta por este contenedor es más fácil de usar que la funcionalidad de cuatro proveedores de servicios independientes. La funcionalidad del contenedor se puede dividir en cuatro áreas principales:

-   Servicios de autenticación de tarjeta inteligente, como obtener desafío y autenticación de tarjeta.
-   Acceso a archivos de tarjeta inteligente o servicios del sistema de archivos, como abrir, cerrar, leer y escribir.
-   Administración de tarjetas inteligentes, como adjuntar y separar.
-   Servicios de comprobación de tarjetas inteligentes, como comprobar y cambiar código.

> [!Note]  
> Esta especificación puede no estar disponible en algunos idiomas y países o regiones.

 

La funcionalidad es específica del tipo de tarjeta que se va a usar (qué funciones admite la tarjeta, protocolos, etc.) y será diferente para cada tarjeta.

El contenedor de ejemplo de Microsoft SCardCOM utiliza la biblioteca COM ATL para implementar un contenedor simple y diseñar una plantilla para otros contenedores. Implementa las interfaces siguientes.



| Interfaz u objeto                                     | Descripción                         |
|---------------------------------------------------------|-------------------------------------|
| [**ISCardAuth**](iscardauth.md)<br/>             | Servicios de autenticación.<br/> |
| [**ISCardFileAccess**](iscardfileaccess.md)<br/> | Servicios del sistema de archivos.<br/>    |
| [**ISCardManage**](iscardmanage.md)<br/>         | Servicios de administración.<br/>     |
| [**ISCardVerify**](iscardverify.md)<br/>         | Servicios de comprobación.<br/>   |



 

> [!Note]  
> El ejemplo SCardCOM se proporciona únicamente como ejemplo de implementación de las interfaces contenedoras. Para evitar el conflicto de nombres de DLL con otros proveedores, no debe utilizar SCardCOM.dll como nombre de los archivos DLL que cree.

 

El siguiente es un uso típico del contenedor del proveedor. En este ejemplo se utiliza la interfaz [**ISCardManage**](iscardmanage.md) para crear instancias de las interfaces que se van a encapsular en el proveedor de servicios y la interfaz [**ISCardVerify**](iscardverify.md) para comprobar su funcionamiento.

**Para compilar un proveedor de servicios de contenedor**

1.  Cree una instancia de la interfaz [**ISCardManage**](iscardmanage.md) . Use esta interfaz para crear una instancia de interfaces requeridas (por ejemplo, [**ISCardFileAccess**](iscardfileaccess.md) o [**ISCardVerify**](iscardverify.md)). Al crear estas interfaces, también se crearán las interfaces COM de bajo nivel correspondientes.
2.  Adjunte o conéctese a una tarjeta a través del método [**ISCardManage**](iscardmanage.md) adecuado.
3.  Realizar las operaciones necesarias a través del método [**ISCardVerify**](iscardverify.md) adecuado (que puede llamar a varios métodos y interfaces com de bajo nivel para completarse).
4.  Repita el procedimiento para otras operaciones.
5.  Liberar al finalizar.

El nombre de la interfaz COM y el identificador de interfaz (GUID) no deben cambiar de los utilizados en el contenedor de código o de ejemplo. Sin embargo, el GUID de clase (es decir, donde reside una implementación real de una interfaz) debe cambiarse de los usados. Esto es especialmente importante cuando se implementa un contenedor de proveedores. Un ejemplo sería el uso de varios contenedores de proveedor en un equipo determinado. Estos contenedores deben implementar las mismas interfaces COM, pero siempre usarán distintas estrategias de implementación. Por lo tanto, se requieren diferentes clases (y identificadores de clase).

 

 




