---
title: Introducción al código
description: La ilustración siguiente es una representación conceptual de los bloques de código necesarios para implementar el componente de proveedor de ejemplo ADSI.
ms.assetid: b353c2d9-ef86-4e4c-ac00-4756fc9ec57d
ms.tgt_platform: multiple
keywords:
- Información general sobre el código de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc23f4a3a51c33f24748347a2941bc09dbda8bc3bd99d133f99d0377eb0bda90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118017735"
---
# <a name="code-overview"></a>Introducción al código

La ilustración siguiente es una representación conceptual de los bloques de código necesarios para implementar el componente de proveedor de ejemplo ADSI. Cada sección se describe en la ilustración siguiente. Los programadores COM experimentados pueden encontrar que esta es una introducción adecuada del componente de proveedor de ejemplo. Para obtener más información, vea [Detalles del código](code-details.md).

![implementación del proveedor de ejemplo](images/dssmco.png)

Los siguientes elementos numerados corresponden a los elementos de bloque de la ilustración.

1.  Cargar el archivo DLL (Libmain.cpp, Guid.cpp). Punto de entrada del archivo DLL. Las definiciones de objetos estáticos del generador de clases para los dos objetos de proveedor: Guid.cpp contiene las definiciones de CLSID para las implementaciones de los distintos objetos de componente de proveedor de ejemplo.
2.  Generador de clases de objeto de proveedor y código de creación (Cprovcf.cpp, Cprov.cpp, Stdfact.cpp). El objeto de proveedor es el objeto que admite [**IParseDisplayName**](/windows/win32/api/oleidl/nn-oleidl-iparsedisplayname) durante las operaciones de enlace de moniker, como se describe en Búsqueda y enlace en el componente de proveedor de ejemplo.
3.  Enlace a un objeto (Getobj.cpp). Este código llama al analizador para comprobar que el ADsPath especificado es sintácticamente correcto y, a continuación, realiza cualquier asignación necesaria desde ADsPath a la ruta de acceso del servicio de directorio nativo para el elemento que se crea como un objeto Active Directory. Busca la definición de esquema para este tipo de objeto y rellena las propiedades obligatorias. Después de crear el Active Directory, se recupera un puntero de interfaz a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para el autor de la llamada.
4.  Analizador del espacio de nombres del proveedor (Parse.cpp). Este es el código invocado por el elemento 3. El analizador comprueba que la cadena ADsPath pasada es sintácticamente correcta para su propio espacio de nombres.
5.  Generador de clases, creación y enumeración para el objeto de espacio de nombres (Cnamcf.cpp, Cnamesp.cpp, Cenumns.cpp). El objeto de espacio de nombres es un objeto contenedor que se puede enumerar para buscar todos los objetos de nodo raíz de este espacio de nombres.
6.  Generador de clases y código de creación para un objeto Active Directory genérico y generador de clases, código de creación y enumeración para un objeto contenedor de ADs genérico (Cgenobj.cpp, Cenumobj.cpp, Common.cpp, Core.cpp). Este código se ejecuta cuando se crea Active Directory objeto .
7.  Filtrado y enumeración de variants (Cenumvar.cpp, Object.cpp). Cuando se administra una colección de elementos VARIANT de un solo tipo en ADSI, se usa este código.
8.  Globals (Globals.cpp). Aquí se definen las palabras clave de espacio de nombres, las estructuras de asignación de sintaxis de formatos de datos nativos al tipo VARIANT de Automatización de ADs.
9.  Serialización/desmarque de datos (Pack.cpp, Property.cpp, Smpoper.cpp). La conversión de formatos de datos nativos al conjunto admitido de tipos VARIANT de Automation se produce cuando las propiedades de un objeto se cargan en la caché de propiedades. Se debe realizar otro control especial de los datos cuando las estructuras con punteros se copian, eliminan o se mueven en memoria.
10. Caché de propiedades (Cprops.cpp). Las propiedades de almacenamiento en caché son una característica del entorno ADSI. Los [**métodos IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo), [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex)y [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) actúan en la caché de propiedades.
11. Administración de memoria (Memory.cpp). El uso de un conjunto de funciones de memoria para asignar y liberar memoria permite que el componente de proveedor de ejemplo realice un seguimiento del uso de memoria y detenga las pérdidas de memoria.
12. Administración y objetos de esquema (Cschobj.cpp, Cprpobj.cpp, Cclsobj.cpp, Cenumsch.cpp). Esto incluye rutinas para crear, administrar y enumerar los objetos de esquema. Esto incluye objetos de clase de esquema, objetos de propiedad y objetos de sintaxis, además de poder enumerar el objeto contenedor de clase de esquema.
13. Llamadas específicas del sistema operativo (RegDSAPI.cpp). Esto incluye todas las llamadas que hacen referencia al sistema operativo nativo. Entre otras funciones, incluyen funciones que abren, cierran, leen y modifican objetos, así como aquellos que acceden a los datos de esquema y propiedad. El componente de proveedor de ejemplo simuló una jerarquía de directorios mediante el Registro. Solo los nombres de función deben ser de gran interés para un escritor de proveedores.
14. [**Implementación de IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (Cdispmgr.cpp). Este código tiene acceso a los datos de la biblioteca de tipos para permitir que los métodos de interfaz se invoque de una manera compatible con Automation.

 

 