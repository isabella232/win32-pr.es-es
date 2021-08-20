---
title: Bibliotecas de tipos, COM y DCOM
description: El Modelo de objetos componentes (COM) y el Modelo de objetos componentes distribuidos (DCOM) usan llamadas a procedimiento remoto (RPC) para permitir que los objetos de componentes distribuidos se comuniquen entre sí.
ms.assetid: 7bade397-676e-43be-82f4-b23cd768fd16
keywords:
- interfaces MIDL, COM
- interfaces MIDL , DCOM
- interfaces MIDL, bibliotecas de tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0997d2a61fef3e2bc46f4539dca2ecd67d8de385d402e5e9c862b267b697b3cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991765"
---
# <a name="com-dcom-and-type-libraries"></a>Bibliotecas de tipos, COM y DCOM

El Modelo de objetos componentes (COM) y el Modelo de objetos componentes distribuidos (DCOM) usan llamadas a procedimiento remoto (RPC) para permitir que los objetos de componentes distribuidos se comuniquen entre sí. Por lo tanto, una interfaz COM o DCOM define la identidad y las características externas de un objeto COM. Forma los medios por los que los clientes pueden obtener acceso a los métodos y datos de un objeto. Con DCOM, este acceso es posible independientemente de si los objetos existen en el mismo proceso, en procesos diferentes en la misma máquina o en máquinas diferentes. Al igual que con las interfaces cliente/servidor RPC, un objeto COM o DCOM puede exponer su funcionalidad de varias maneras diferentes y a través de varias interfaces.

## <a name="type-library"></a>Biblioteca de tipos

Una biblioteca de tipos (.tlb) es un archivo binario que almacena información sobre las propiedades y los métodos de un objeto COM o DCOM en un formato al que pueden acceder otras aplicaciones en tiempo de ejecución. Mediante una biblioteca de tipos, una aplicación o explorador puede determinar qué interfaces admite un objeto e invocar los métodos de interfaz de un objeto. Esto puede ocurrir incluso si las aplicaciones de objeto y cliente se escribieron en distintos lenguajes de programación. El entorno en tiempo de ejecución com/DCOM también puede usar una biblioteca de tipos para proporcionar serialización automática entre departamentos, entre procesos y entre máquinas para las interfaces descritas en las bibliotecas de tipos.

## <a name="characteristics-of-an-interface"></a>Características de una interfaz

Defina las características de una interfaz en un archivo de definición de interfaz (IDL) y un archivo de configuración de aplicación (ACF) opcional:

-   El archivo IDL especifica las características de las interfaces de la aplicación en la conexión, es decir, cómo se transmiten los datos entre el cliente y el servidor, o entre objetos COM.
-   El archivo ACF especifica las características de la interfaz, como los identificadores de enlace, que pertenecen solo al entorno operativo local. El archivo ACF también puede especificar cómo serializar y transmitir una estructura de datos compleja en un formato independiente del equipo.

Para obtener más información sobre los archivos IDL y ACF, vea [The IDL and ACF Files](/windows/desktop/Rpc/the-idl-and-acf-files).

Los archivos IDL y ACF son scripts escritos en Lenguaje de definición de interfaz de Microsoft (MIDL), que es la implementación y extensión de Microsoft del lenguaje de definición de interfaz (IDL) de OSF-DCE. Las extensiones de Microsoft para el lenguaje IDL permiten crear interfaces COM y bibliotecas de tipos. El compilador, Midl.exe, usa estos scripts para generar archivos de encabezado y código auxiliar del lenguaje C, así como archivos de biblioteca de tipos.

## <a name="the-midl-compiler"></a>El compilador MIDL

Según el contenido del archivo IDL, el compilador de MIDL generará cualquiera de los siguientes archivos.

Un archivo proxy/stub en lenguaje C, un archivo de identificador de interfaz, un archivo de datos DLL y un archivo de encabezado relacionado para una interfaz COM personalizada. El compilador MIDL genera estos archivos cuando encuentra el atributo de objeto en una lista de atributos de interfaz. Para obtener información más detallada sobre estos archivos, vea [Archivos generados para una interfaz COM](files-generated-for-a-com-interface.md).

Un archivo de biblioteca de tipos compilado (.tlb) y un archivo de encabezado relacionado. MIDL genera estos archivos cuando encuentra una instrucción [**de biblioteca**](library.md) en el archivo IDL. Para obtener información general sobre las bibliotecas de tipos, vea Contenido de [una biblioteca de tipos](/previous-versions/windows/desktop/automat/contents-of-a-type-library)en la Referencia del programador de Automation.

Archivos de código auxiliar de cliente y servidor del lenguaje C/C++, así como un archivo de encabezado relacionado para una interfaz RPC. Estos archivos se generan cuando hay interfaces en el archivo IDL que no tienen el [**atributo de**](object.md) objeto. Para obtener información general sobre los archivos de código auxiliar y de encabezado, vea [Procedimiento de compilación general](/windows/desktop/Rpc/general-build-procedure). Para obtener información más detallada, vea [Archivos generados para una interfaz RPC.](files-generated-for-an-rpc-interface.md)

 

 