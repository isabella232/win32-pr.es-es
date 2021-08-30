---
description: En Windows Vista y Windows Server 2008, las ubicaciones predeterminadas de los datos de usuario y los datos del sistema han cambiado.
ms.assetid: 78679851-91f5-447f-8580-12cbf0323fb8
title: Puntos de unión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5415e3b7a01434c5fa49d309f1b2192dbd9c9c62475c9fada1501337de7ddc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866335"
---
# <a name="junction-points"></a>Puntos de unión

En Windows Vista y Windows Server 2008, las ubicaciones predeterminadas de los datos de usuario y los datos del sistema han cambiado. Por ejemplo, los datos de usuario almacenados anteriormente en el directorio %SystemDrive% Documents y Configuración ahora se almacenan en el \\ directorio %SystemDrive% \\ Users. Por compatibilidad con versiones anteriores, las ubicaciones antiguas tienen puntos de unión que apuntan a las nuevas ubicaciones. Por ejemplo, C: \\ Documentos y Configuración es ahora un punto de unión que apunta a C: \\ Usuarios. Las aplicaciones de copia de seguridad deben ser capaces de realizar copias de seguridad y restaurar puntos de unión.

Estos puntos de unión se pueden identificar de la siguiente manera:

-   Tienen establecidos los atributos \_ FILE ATTRIBUTE \_ REPARSE POINT, FILE ATTRIBUTE HIDDEN y FILE ATTRIBUTE \_ \_ \_ \_ \_ SYSTEM.
-   También tienen sus listas de control de acceso (ACL) establecidas para denegar el acceso de lectura a todos los usuarios.

Las aplicaciones que llaman a una ruta de acceso específica pueden atravesar estos puntos de unión si tienen los permisos necesarios. Sin embargo, los intentos de enumerar el contenido de los puntos de unión provocarán errores. Es importante que las aplicaciones de copia de seguridad no atraviesen estos puntos de unión ni intenten realizar copias de seguridad de los datos debajo de ellos por dos motivos:

-   Si lo hace, la aplicación de copia de seguridad puede hacer una copia de seguridad de los mismos datos más de una vez.
-   También puede dar lugar a ciclos (referencias circulares).

## <a name="per-user-junctions-and-system-junctions"></a>Per-User uniones y uniones del sistema

Los puntos de unión que se usan para proporcionar virtualización de archivos y registros en Windows Vista y Windows Server 2008 se pueden dividir en dos clases: uniones por usuario y uniones del sistema.

Las uniones por usuario se crean dentro del perfil de cada usuario individual para proporcionar compatibilidad con versiones anteriores para las aplicaciones de usuario. El punto de unión en C: Nombre de usuario Mis documentos usuarios que apunta a C: Usuarios nombre de usuario Documentos es un ejemplo de una \\ \\  \\ \\ unión por \\  \\ usuario. El servicio de perfiles crea uniones por usuario cuando se crea el perfil del usuario.

Las otras uniones son uniones del sistema que no residen en el directorio Users username (Nombre de usuario \\ *de* usuarios). Entre los ejemplos de uniones del sistema se incluyen:

-   Documentos y Configuración
-   Uniones dentro de los perfiles Todos los usuarios, Público y Usuario predeterminado

Las uniones del sistema se crean userenv.dll cuando se invocan mediante Windows Welcome (también denominada experiencia de máquina lista para usar o mOOBE).

> [!Note]  
> Si el usuario cambia el idioma del sistema a un idioma distinto del inglés, los puntos de unión por usuario y sistema se crearán con nombres localizados.

 

 

 



