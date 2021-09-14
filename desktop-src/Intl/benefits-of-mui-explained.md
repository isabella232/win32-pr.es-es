---
description: Ventajas de LA EXPLICACIÓN explicada
ms.assetid: 5b9851e0-4354-4088-b099-0f5f5fac4a35
title: Ventajas de LA EXPLICACIÓN explicada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1915e58e28ac9c7b3a43cc0ba217b8d56657c1b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274844"
---
# <a name="benefits-of-mui-explained"></a>Ventajas de LA EXPLICACIÓN explicada

-   [Ventajas de LAS APLICACIONES para desarrolladores](#mui-benefits-for-developers)
-   [Ventajas de LA CONVERSIÓN para empresas](#mui-benefits-for-enterprises)
-   [Ventajas de LA CLAVE para OEM](#mui-benefits-for-oems)

## <a name="mui-benefits-for-developers"></a>Ventajas de LAS APLICACIONES para desarrolladores

Hay muchas maneras posibles de implementar una solución DE ACUERDO en aplicaciones, pero cada posibilidad es una variación de uno de los tres métodos básicos:

1.  Compilar un archivo binario (con recursos integrados) para cada lenguaje. Este es el *estándar de facto* para las aplicaciones heredadas, ya que este es el modelo principal compatible con herramientas de desarrollo estándar como Microsoft Visual Studio. Este modelo requiere varios archivos binarios para varios lenguajes y tiene limitaciones con respecto a la implementación de una sola imagen y a escenarios multilingües. Debe tenerse en cuenta que las aplicaciones desarrolladas con este modelo seguirán funcionando en Windows Vista y que se proporcionan herramientas que ayudan a los desarrolladores a pasar de este modelo al modelo más moderno descrito en el tercer método.
2.  Tener un binario de núcleo neutro del lenguaje con una biblioteca de vínculos dinámicos (DLL) de recursos de varios idiomas. Este modelo es definitivamente fácil de USAR, pero dificulta la actualización de los archivos binarios de recursos para dar cabida a nuevos lenguajes. Supongamos que, además del inglés, el francés y el japonés, también quiere admitir el alemán. Es necesario proporcionar e implementar un nuevo archivo binario de recursos para los usuarios que no necesitan necesariamente alemán.
3.  Tener un binario de núcleo neutro del lenguaje con un conjunto de archivos DLL de recursos por idioma. Esta es la manera en que el propio sistema operativo se implementa en Windows Vista y se anima a los desarrolladores a usar este modelo para las aplicaciones, ya que ofrece más que los dos modelos anteriores.

Antes de la Windows Vista, la falta de compatibilidad integrada con este último modelo hacía que fuera difícil de adoptar. Sin embargo, esto ha cambiado y las ventajas de este modelo son numerosas y lo convierten en un excelente modelo para sus aplicaciones:

-   Las aplicaciones se pueden convertir en multilingües y pueden comportarse de la misma manera que Windows Vista, lo que proporciona una experiencia de lenguaje de presentación coherente para los usuarios.
-   La flexibilidad aumenta a la hora de publicar idiomas adicionales para una aplicación. Se pueden publicar idiomas adicionales independientemente del código principal, lo que significa que se puede agregar compatibilidad con nuevos lenguajes con el tiempo según sea necesario.
-   El costo se reduce en la creación y el mantenimiento de más versiones de lenguaje.
-   Los OEM y las empresas pueden integrar fácilmente las aplicaciones en su imagen de EQUIPO globalizado, lista para su envío a distintos países.
-   Hay disponibles herramientas e instrucciones que le ayudarán a migrar la aplicación al Windows vista DE VISTA. En concreto, MSDN proporciona un [conjunto significativo de documentación](multilingual-user-interface.md) sobre LA NUBE.

## <a name="mui-benefits-for-enterprises"></a>Ventajas de LA CONVERSIÓN para empresas

LA CARACTERÍSTICA ofrece dos ventajas principales para las empresas:

-   Instalación de una sola imagen: LA CONVERSIÓN permite a las empresas implantar, admitir y mantener la misma imagen en todo el mundo (o cualquier parte de ella) con una sola instalación. Windows Vista amplía el lanzamiento de una sola imagen del sistema operativo para que las aplicaciones empresariales también se puedan implementar como parte de la misma imagen.
-   Compatibilidad con escritorios multilingües: se pueden instalar varios paquetes de idioma de interfaz de usuario localizados en un escritorio, lo que permite que varios usuarios compartan un solo escritorio mientras siguen usando sus propios idiomas de interfaz de usuario preferidos. Esto también se aplica a los equipos públicos, que necesitan un tratamiento igual para todos los idiomas oficialmente hablados (por ejemplo, en Canadá y en la Unión Europea) y en los equipos compartidos para los usuarios móviles.

## <a name="mui-benefits-for-oems"></a>Ventajas de LA CLAVE para OEM

La principal ventaja de los OEM es la instalación de una sola imagen que HABILITA LAN, ya que permite crear imágenes que contengan todos los idiomas necesarios para dirigirse de forma eficaz a una zona geográfica y retrasar la elección del idioma a la instalación inicial del equipo por parte del usuario. En concreto, esto permite una administración más eficaz del inventario de OEM.

Al proporcionar compatibilidad con LAME para aplicaciones, Windows Vista también permite que los OEM proporcionen aplicaciones de valor añadido en sus imágenes mientras se benefician de la instalación de una sola imagen, siempre y cuando estas aplicaciones estén habilitadas para LA NUBE.

 

 



