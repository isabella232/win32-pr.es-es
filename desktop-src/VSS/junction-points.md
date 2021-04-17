---
description: En Windows Vista y Windows Server 2008, las ubicaciones predeterminadas para los datos de usuario y los datos del sistema han cambiado.
ms.assetid: 78679851-91f5-447f-8580-12cbf0323fb8
title: Puntos de Unión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f1823c67e2c6b95ae366b7604054b47305062e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697006"
---
# <a name="junction-points"></a>Puntos de Unión

En Windows Vista y Windows Server 2008, las ubicaciones predeterminadas para los datos de usuario y los datos del sistema han cambiado. Por ejemplo, los datos de usuario que se almacenaron previamente en el directorio% SystemDrive% \\ Documents and Settings se almacenan ahora en el directorio% SystemDrive% \\ users. Por compatibilidad con versiones anteriores, las ubicaciones anteriores tienen puntos de Unión que apuntan a las nuevas ubicaciones. Por ejemplo, C: \\ Documents and Settings es ahora un punto de Unión que apunta a C: \\ users. Las aplicaciones de copia de seguridad deben ser capaces de realizar copias de seguridad y restaurar puntos de Unión.

Estos puntos de Unión se pueden identificar de la manera siguiente:

-   Tienen el atributo de \_ archivo \_ punto de reanálisis \_ , \_ atributo de archivo \_ oculto y \_ conjunto de atributos de archivo del sistema de atributos de archivo \_ .
-   También tienen sus listas de control de acceso (ACL) configuradas para denegar el acceso de lectura a todos.

Las aplicaciones que llaman a una ruta de acceso específica pueden atravesar estos puntos de unión si tienen los permisos necesarios. Sin embargo, los intentos de enumerar el contenido de los puntos de Unión producirán errores. Es importante que las aplicaciones de copia de seguridad no atraviesen estos puntos de unión o intenten hacer una copia de seguridad de los mismos por dos motivos:

-   Si lo hace, la aplicación de copia de seguridad puede hacer una copia de seguridad de los mismos datos más de una vez.
-   También puede conducir a ciclos (referencias circulares).

## <a name="per-user-junctions-and-system-junctions"></a>Uniones de Per-User y uniones del sistema

Los puntos de Unión que se usan para proporcionar la virtualización de archivos y del registro en Windows Vista y Windows Server 2008 se pueden dividir en dos clases: uniones por usuario y uniones del sistema.

Las uniones por usuario se crean dentro de cada perfil de usuario individual para proporcionar compatibilidad con versiones anteriores para las aplicaciones de usuario. El punto de Unión en C: \\ users \\ *nombreDeUsuario* \\ Mis documentos que señala a c: \\ users \\ *nombreDeUsuario* \\ Documents es un ejemplo de una Unión por usuario. El servicio de perfil crea las uniones por usuario cuando se crea el perfil del usuario.

Las demás uniones son uniones del sistema que no residen en el directorio users \\ *username* . Entre los ejemplos de uniones del sistema se incluyen:

-   Documentos y configuración
-   Uniones dentro de los perfiles de usuario todos los usuarios, públicos y predeterminados

Las uniones del sistema se crean mediante userenv.dll cuando la bienvenida de Windows la invoca (también se conoce como la máquina rápida o mOOBE).

> [!Note]  
> Si el usuario cambia el idioma del sistema a un idioma distinto del inglés, los puntos de Unión por usuario y sistema se crearán con nombres localizados.

 

 

 



