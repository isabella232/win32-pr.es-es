---
description: El almacenamiento protegido proporciona a las aplicaciones una interfaz para almacenar los datos de usuario que deben mantenerse seguros o que no se pueden modificar.
ms.assetid: 85c1a009-c4f7-4b5a-ad96-6845a4e80de9
title: PStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9d291b911c351cce10827b7937c6a474b7c570
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666159"
---
# <a name="pstore"></a>PStore

\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

El almacenamiento protegido proporciona a las aplicaciones una interfaz para almacenar los datos de usuario que deben mantenerse seguros o que no se pueden modificar.

Las unidades de datos almacenadas se denominan elementos. La estructura y el contenido de los datos almacenados son opacos para el sistema de almacenamiento protegido. El acceso a los elementos está sujeto a la confirmación en función de un estilo de seguridad definido por el usuario, que especifica qué confirmación es necesaria para obtener acceso a los datos, por ejemplo, si se requiere una contraseña. Además, el acceso a los elementos está sujeto a un conjunto de reglas de acceso. Hay una regla de acceso para cada modo de acceso: por ejemplo, de lectura/escritura. Los conjuntos de reglas de acceso se componen de cláusulas de acceso. Actualmente se admiten dos tipos de cláusulas de acceso: Authenticode y comprobación binaria del llamador. Normalmente, en el momento de la configuración de la aplicación, se proporciona un mecanismo para permitir que una nueva aplicación solicite al usuario el acceso a los elementos que ha creado anteriormente otra aplicación.

Los elementos se identifican de forma única mediante la combinación de una clave, tipo, subtipo y nombre. La clave es una constante que especifica si el elemento es global para este equipo o solo está asociado a este usuario. El nombre es una cadena, que suele elegir el usuario. El tipo y el subtipo son **GUID**, normalmente especificados por la aplicación. La información adicional sobre los tipos y subtipos se mantiene en el registro del sistema e incluye atributos como el nombre para mostrar y las sugerencias de la interfaz de usuario. En el caso de los subtipos, el tipo primario es fijo y se incluye en el registro del sistema como un atributo. Los elementos de grupo de tipo se usan para un propósito común: por ejemplo, pago o identificación. Los elementos del grupo de subtipos comparten un formato de datos común.

## <a name="in-this-section"></a>En esta sección

-   [**IEnumPStoreItems**](ienumpstoreitems.md)
-   [**IEnumPStoreProviders**](ienumpstoreproviders.md)
-   [**IEnumPStoreTypes**](ienumpstoretypes.md)
-   [**IPStore**](ipstore.md)
-   [**PStoreCreateInstance**](pstorecreateinstance.md)
-   [**PStoreEnumProviders**](pstoreenumproviders.md)
-   [**PStore (constantes)**](pstore-constants.md)
-   [**PStore (tipos)**](pstore-types.md)

 

 
