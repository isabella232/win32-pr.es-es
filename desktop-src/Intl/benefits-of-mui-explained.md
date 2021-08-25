---
description: Ventajas de la EXPLICACIÓN explicada
ms.assetid: 5b9851e0-4354-4088-b099-0f5f5fac4a35
title: Ventajas de la EXPLICACIÓN explicada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971f66ef7fc094912e87d7e9ab77284fecb0931d9222e6910931b281b6308286
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829705"
---
# <a name="benefits-of-mui-explained"></a>Ventajas de la EXPLICACIÓN explicada

-   [Ventajas de MUI para desarrolladores](#mui-benefits-for-developers)
-   [Ventajas de TOS para empresas](#mui-benefits-for-enterprises)
-   [Ventajas de TOM para OEM](#mui-benefits-for-oems)

## <a name="mui-benefits-for-developers"></a>Ventajas de MUI para desarrolladores

Hay muchas maneras posibles de implementar una solución DE EXTENSIÓN en aplicaciones, pero cada posibilidad es una variación de uno de los tres métodos básicos:

1.  Compilar un archivo binario (con recursos integrados) para cada lenguaje. Este es el *estándar de facto* para las aplicaciones heredadas, ya que este es el modelo principal compatible con herramientas de desarrollo estándar como Microsoft Visual Studio. Este modelo requiere varios archivos binarios para varios idiomas y tiene limitaciones con respecto a la implementación de una sola imagen y a escenarios multilingües. Debe tenerse en cuenta que las aplicaciones desarrolladas con este modelo seguirán funcionando en Windows Vista y que se proporcionan herramientas que ayudan a los desarrolladores a pasar de este modelo al modelo más moderno descrito en el tercer método.
2.  Tener un binario de núcleo neutro del lenguaje con una biblioteca de vínculos dinámicos (DLL) de recursos de varios idiomas. Definitivamente, este modelo es descriptivo para MUI, pero dificulta la actualización de los archivos binarios de recursos para dar cabida a nuevos idiomas. Supongamos que, además de inglés, francés y japonés, también quiere admitir el alemán. Es necesario proporcionar e implementar un archivo binario de recursos completamente nuevo para los usuarios que no necesitan necesariamente alemán.
3.  Tener un binario de núcleo neutro del lenguaje con un conjunto de archivos DLL de recursos por idioma. Esta es la forma en que el propio sistema operativo se implementa en Windows Vista y se recomienda a los desarrolladores que usen este modelo para las aplicaciones, ya que ofrece más que los dos modelos anteriores.

Antes de la Windows Vista, la falta de compatibilidad integrada con este último modelo hacía que fuera difícil de adoptar. Sin embargo, esto ha cambiado y las ventajas de este modelo son numerosas y lo convierten en un modelo excelente para las aplicaciones:

-   Las aplicaciones se pueden convertir en varios idiomas y pueden comportarse de la misma manera que Windows Vista, lo que proporciona una experiencia de lenguaje de presentación coherente para los usuarios.
-   La flexibilidad aumenta a la hora de publicar idiomas adicionales para una aplicación. Se pueden publicar idiomas adicionales independientemente del código principal, lo que significa que la compatibilidad con nuevos idiomas se puede agregar con el tiempo según sea necesario.
-   El costo se reduce en la creación y el mantenimiento de más versiones de lenguaje.
-   Los OEM y las empresas pueden integrar fácilmente aplicaciones en su imagen de PC globalizada, lista para su envío a distintos países.
-   Hay disponibles herramientas e instrucciones que le ayudarán a migrar la aplicación al modelo Windows VISTA DE VISTA. En concreto, MSDN proporciona un [conjunto significativo de documentación](multilingual-user-interface.md) sobre MUI.

## <a name="mui-benefits-for-enterprises"></a>Ventajas de TOS para empresas

MUI ofrece dos ventajas principales para las empresas:

-   Instalación de una sola imagen: MUI permite a las empresas implantar, admitir y mantener la misma imagen en todo el mundo (o cualquier parte de ella) con una sola instalación. Windows Vista amplía el lanzamiento de una sola imagen del sistema operativo para que las aplicaciones empresariales también se puedan implementar como parte de la misma imagen.
-   Compatibilidad con escritorios multilingües: se pueden instalar varios paquetes de idioma de interfaz de usuario localizados en un escritorio, lo que permite a varios usuarios compartir un único escritorio mientras siguen usando sus propios idiomas de interfaz de usuario preferidos. Esto también se aplica a los equipos públicos, que necesitan un tratamiento igual para todos los idiomas oficialmente hablados (por ejemplo, en Canadá y en la Unión Europea) y en equipos compartidos para usuarios móviles.

## <a name="mui-benefits-for-oems"></a>Ventajas de TOM para OEM

La principal ventaja para los OEM es la instalación de una sola imagen que habilita LAN, ya que permite crear imágenes que contengan todos los idiomas necesarios para dirigirse de forma eficaz a una zona geográfica y retrasar la elección de idioma a la instalación inicial del equipo por parte del usuario. En concreto, esto permite una administración más eficaz del inventario de oem.

Al proporcionar compatibilidad con MUI para las aplicaciones, Windows Vista también permite que los OEM proporcionen aplicaciones de valor añadido en sus imágenes mientras se benefician de la instalación de una sola imagen, siempre y cuando estas aplicaciones estén habilitadas para MUI.

 

 



