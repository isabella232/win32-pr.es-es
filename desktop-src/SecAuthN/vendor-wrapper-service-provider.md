---
description: El propósito del contenedor del proveedor es encapsular y usar las interfaces COM de bajo nivel (proporcionadas por los fabricantes de tarjetas inteligentes) para una tarjeta inteligente determinada. Microsoft no proporciona estas interfaces.
ms.assetid: 7bc26f7b-c355-448a-9f23-4ccfffea2fef
title: Proveedor de servicios contenedor de proveedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b7d22fea8e450111e1611f2ec069697c229a32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160888"
---
# <a name="vendor-wrapper-service-provider"></a>Proveedor de servicios contenedor de proveedores

El propósito del contenedor del proveedor es encapsular y usar las interfaces COM de bajo nivel (proporcionadas por los fabricantes de tarjetas inteligentes) para una tarjeta inteligente determinada. Microsoft no proporciona estas interfaces.

![contenedor del proveedor](images/scspart1.png)

Como se describe en la parte 6 de la especificación de interoperabilidad para los *iccs* y los sistemas informáticos personales (consulte las especificaciones en ), la funcionalidad expuesta por este contenedor es más fácil de usar que la funcionalidad de cuatro proveedores de servicios [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) independientes. La funcionalidad del contenedor se puede dividir en cuatro áreas principales:

-   Servicios de autenticación de tarjeta inteligente, como obtener desafío y autenticación de tarjeta.
-   Acceso a archivos de tarjeta inteligente o servicios del sistema de archivos, como abrir, cerrar, leer y escribir.
-   Administración de tarjetas inteligentes, como adjuntar y separar.
-   Servicios de verificación de tarjeta inteligente, como comprobar y cambiar código.

> [!Note]  
> Es posible que esta especificación no esté disponible en algunos idiomas y países o regiones.

 

La funcionalidad es específica del tipo de tarjeta que se usa (qué funciones admite la tarjeta, protocolos, entre otros) y será diferente para cada tarjeta.

El contenedor de ejemplo de Microsoft SCardCOM usa la biblioteca COM ATL para implementar un contenedor simple y crear una plantilla para otros contenedores. Implementa las interfaces siguientes.



| Interfaz u objeto                                     | Descripción                         |
|---------------------------------------------------------|-------------------------------------|
| [**ISCardAuth**](iscardauth.md)<br/>             | Servicios de autenticación.<br/> |
| [**ISCardFileAccess**](iscardfileaccess.md)<br/> | Servicios del sistema de archivos.<br/>    |
| [**ISCardManage**](iscardmanage.md)<br/>         | Servicios de administración.<br/>     |
| [**ISCardVerify**](iscardverify.md)<br/>         | Servicios de verificación.<br/>   |



 

> [!Note]  
> El ejemplo de SCardCOM solo se proporciona como ejemplo de implementación de las interfaces contenedoras. Para evitar la colisión de nombres de DLL con otros proveedores, no debe usar SCardCOM.dll como nombre de los archivos DLL que cree.

 

A continuación se muestra un uso típico del contenedor del proveedor. En este ejemplo se usa la interfaz [**ISCardManage**](iscardmanage.md) para crear instancias de las interfaces que se encapsularán en el proveedor de servicios y la interfaz [**ISCardVerify**](iscardverify.md) para comprobar su funcionamiento.

**Para compilar un proveedor de servicios contenedor**

1.  Cree una instancia de la [**interfaz ISCardManage.**](iscardmanage.md) Use esta interfaz para crear una instancia de las interfaces necesarias (por ejemplo, [**ISCardFileAccess**](iscardfileaccess.md) o [**ISCardVerify).**](iscardverify.md) Al crear estas interfaces, también se crearían las interfaces COM de bajo nivel correspondientes.
2.  Adjunte o conéctese a una tarjeta a través del [**método ISCardManage**](iscardmanage.md) adecuado.
3.  Realice las operaciones necesarias a través del método [**ISCardVerify**](iscardverify.md) adecuado (que puede llamar a varias interfaces y métodos COM de bajo nivel para completarse).
4.  Repita esta operación para otras operaciones.
5.  Liberar cuando haya finalizado.

El nombre de interfaz COM y el identificador de interfaz (GUID) no deben cambiar de los usados en el contenedor de código o de ejemplo. Sin embargo, el GUID de clase (es decir, donde reside una implementación real de una interfaz) debe cambiarse de los usados. Esto es especialmente importante al implementar un contenedor de proveedor. Un ejemplo sería el uso de varios contenedores de proveedor en un equipo determinado. Estos contenedores deben implementar las mismas interfaces COM, pero siempre usarán estrategias de implementación diferentes. Por lo tanto, se requieren clases diferentes (e iDs de clase).

 

 




