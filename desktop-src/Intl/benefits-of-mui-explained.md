---
description: Ventajas de MUI
ms.assetid: 5b9851e0-4354-4088-b099-0f5f5fac4a35
title: Ventajas de MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1915e58e28ac9c7b3a43cc0ba217b8d56657c1b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082083"
---
# <a name="benefits-of-mui-explained"></a>Ventajas de MUI

-   [Ventajas de MUI para desarrolladores](#mui-benefits-for-developers)
-   [Ventajas de MUI para empresas](#mui-benefits-for-enterprises)
-   [Ventajas de MUI para OEM](#mui-benefits-for-oems)

## <a name="mui-benefits-for-developers"></a>Ventajas de MUI para desarrolladores

Hay muchas formas posibles de implementar una solución de MUI en aplicaciones, pero cada una de ellas es una variación de uno de los tres métodos básicos:

1.  Compilar un binario (con recursos integrados) para cada idioma. Este es el estándar *de facto* para las aplicaciones heredadas, ya que este es el modelo principal compatible con las herramientas de desarrollo estándar como Microsoft Visual Studio. Este modelo requiere varios archivos binarios para varios idiomas y tiene limitaciones en cuanto a la implementación de una sola imagen y escenarios multilingües. Debe tenerse en cuentan que las aplicaciones desarrolladas con este modelo seguirán funcionando en Windows Vista y que se proporcionarán herramientas que ayudan a los desarrolladores a pasar de este modelo al modelo más moderno descrito en el tercer método.
2.  Tener un archivo binario principal independiente del lenguaje con una biblioteca de vínculos dinámicos (DLL) de recursos de varios idiomas. Este modelo es definitivamente compatible con MUI, pero hace que sea difícil actualizar los archivos binarios de recursos para acomodar nuevos idiomas. Supongamos que, además de inglés, francés y japonés, desea admitir también el alemán. Es necesario proporcionar e implementar todo un archivo binario de recurso nuevo en los usuarios que no necesiten necesariamente el alemán.
3.  Tener un binario principal independiente del lenguaje con un conjunto de dll de recursos por idioma. Esta es la forma en que se implementa el sistema operativo en Windows Vista y se recomienda a los desarrolladores que utilicen este modelo para las aplicaciones, ya que ofrece más de los dos modelos anteriores.

Antes de la versión de Windows Vista, la falta de compatibilidad integrada con este último modelo dificultaba la adopción. Sin embargo, esto ha cambiado y las ventajas de este modelo son numerosas y lo convierten en un modelo excelente para las aplicaciones:

-   Las aplicaciones pueden ser multilingües y pueden comportarse de la misma manera que Windows Vista, lo que proporciona una experiencia de lenguaje de visualización coherente para los usuarios.
-   La flexibilidad aumenta en la liberación de idiomas adicionales para una aplicación. Los idiomas adicionales se pueden publicar independientemente del código principal, lo que significa que se puede Agregar a lo largo del tiempo la compatibilidad con nuevos idiomas.
-   El costo se reduce en la creación y el mantenimiento de más versiones de idioma.
-   Los fabricantes de equipos originales (OEM) y las empresas pueden integrar fácilmente aplicaciones en su imagen de equipo globalizada, listas para su envío a distintos países.
-   Están disponibles las herramientas y directrices que le ayudarán a migrar la aplicación al modelo MUI de Windows Vista. En concreto, MSDN proporciona un [conjunto de documentación importante](multilingual-user-interface.md) sobre MUI.

## <a name="mui-benefits-for-enterprises"></a>Ventajas de MUI para empresas

MUI ofrece dos ventajas principales para las empresas:

-   Instalación de una sola imagen: MUI permite que las empresas implementen, admitan y mantengan la misma imagen en todo el mundo (o cualquier parte de ella) con una sola instalación. Windows Vista extiende la implementación de una sola imagen del sistema operativo, de modo que las aplicaciones empresariales también se pueden implementar como parte de la misma imagen.
-   Compatibilidad con escritorios multilingües: se pueden instalar varios paquetes de idioma de interfaz de usuario localizada en un escritorio, lo que permite que varios usuarios compartan un solo escritorio sin dejar de utilizar sus propios idiomas de interfaz de usuario preferidos. Esto también se aplica a los equipos públicos, que necesitan un trato igual para todos los idiomas hablados oficialmente (como podría ser el caso en Canadá y en la Unión Europea) y en equipos compartidos para usuarios móviles.

## <a name="mui-benefits-for-oems"></a>Ventajas de MUI para OEM

La principal ventaja para los OEM es la instalación de imagen única que MUI habilita, ya que permite crear imágenes que contengan todos los idiomas necesarios para tener como destino una zona geográfica de forma eficaz, y para retrasar la elección del idioma a la instalación inicial del equipo del usuario. En concreto, esto permite una administración más eficaz del inventario para los OEM.

Al proporcionar compatibilidad con MUI para las aplicaciones, Windows Vista también permite a los OEM proporcionar aplicaciones de valor agregado en sus imágenes mientras se benefician de la instalación de una sola imagen, siempre y cuando estas aplicaciones estén habilitadas para MUI.

 

 



