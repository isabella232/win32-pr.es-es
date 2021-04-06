---
title: COM, DCOM y bibliotecas de tipos
description: El modelo de objetos componentes (COM) y el modelo de objetos componentes distribuido (DCOM) utilizan llamadas a procedimiento remoto (RPC) para permitir que los objetos de componentes distribuidos se comuniquen entre sí.
ms.assetid: 7bade397-676e-43be-82f4-b23cd768fd16
keywords:
- interfaces MIDL, COM
- interfaces MIDL, DCOM
- interfaces MIDL, bibliotecas de tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f0b21aad9f88f02d8029d478eead50f5501ecc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904568"
---
# <a name="com-dcom-and-type-libraries"></a>COM, DCOM y bibliotecas de tipos

El modelo de objetos componentes (COM) y el modelo de objetos componentes distribuido (DCOM) utilizan llamadas a procedimiento remoto (RPC) para permitir que los objetos de componentes distribuidos se comuniquen entre sí. Por lo tanto, una interfaz COM o DCOM define la identidad y las características externas de un objeto COM. Forma los medios por los que los clientes pueden obtener acceso a los métodos y datos de un objeto. Con DCOM, este acceso es posible independientemente de si los objetos existen en el mismo proceso, en distintos procesos en el mismo equipo o en equipos diferentes. Al igual que con las interfaces cliente/servidor de RPC, un objeto COM o DCOM puede exponer su funcionalidad de varias maneras diferentes y a través de varias interfaces.

## <a name="type-library"></a>Biblioteca de tipos

Una biblioteca de tipos (. tlb) es un archivo binario que almacena información sobre las propiedades y los métodos de un objeto COM o DCOM en un formulario accesible a otras aplicaciones en tiempo de ejecución. Mediante una biblioteca de tipos, una aplicación o explorador puede determinar qué interfaces admite un objeto e invocar los métodos de interfaz de un objeto. Esto puede ocurrir incluso si las aplicaciones cliente y de objeto se escribieron en diferentes lenguajes de programación. El entorno de tiempo de ejecución de COM/DCOM también puede usar una biblioteca de tipos para proporcionar serialización automática entre apartamentos, entre procesos y multiequipo para las interfaces descritas en bibliotecas de tipos.

## <a name="characteristics-of-an-interface"></a>Características de una interfaz

Las características de una interfaz se definen en un archivo de definición de interfaz (IDL) y un archivo de configuración de la aplicación opcional (ACF):

-   El archivo IDL especifica las características de las interfaces de la aplicación en la conexión, es decir, cómo se van a transmitir los datos entre el cliente y el servidor, o entre los objetos COM.
-   El archivo ACF especifica las características de la interfaz, como los identificadores de enlace, que solo pertenecen al entorno operativo local. El archivo ACF también puede especificar cómo calcular las referencias y transmitir una estructura de datos compleja en un formulario independiente de la máquina.

Para obtener más información sobre los archivos IDL y ACF, vea [los archivos IDL y ACF](/windows/desktop/Rpc/the-idl-and-acf-files).

Los archivos IDL y ACF son scripts escritos en Lenguaje de definición de interfaz de Microsoft (MIDL), que es la implementación de Microsoft y la extensión del lenguaje de definición de interfaz (IDL) de OSF-DCE. Las extensiones de Microsoft para el lenguaje IDL permiten crear interfaces COM y bibliotecas de tipos. El compilador, Midl.exe, utiliza estos scripts para generar códigos auxiliares del lenguaje C y archivos de encabezado, así como archivos de biblioteca de tipos.

## <a name="the-midl-compiler"></a>El compilador MIDL

En función del contenido del archivo IDL, el compilador MIDL generará cualquiera de los siguientes archivos.

Un archivo de proxy/código auxiliar de lenguaje C, un archivo de identificador de interfaz, un archivo de datos DLL y un archivo de encabezado relacionado para una interfaz COM personalizada. El compilador MIDL genera estos archivos cuando encuentra el atributo de objeto en una lista de atributos de interfaz. Para obtener información más detallada sobre estos archivos, consulte [archivos generados para una interfaz com](files-generated-for-a-com-interface.md).

Un archivo de biblioteca de tipos (. tlb) compilado y un archivo de encabezado relacionado. MIDL genera estos archivos cuando encuentra una instrucción [**Library**](library.md) en el archivo IDL. Para obtener información general acerca de las bibliotecas de tipos, vea el [contenido de una biblioteca de tipos](/previous-versions/windows/desktop/automat/contents-of-a-type-library), en la referencia del programador de Automation.

Archivos de código auxiliar de cliente y servidor de lenguaje C/C++ y archivo de encabezado relacionado para una interfaz RPC. Estos archivos se generan cuando hay interfaces en el archivo IDL que no tienen el atributo de [**objeto**](object.md) . Para obtener información general sobre el código auxiliar y los archivos de encabezado, consulte [procedimiento de compilación general](/windows/desktop/Rpc/general-build-procedure). Para obtener información más detallada, consulte [archivos generados para una interfaz RPC](files-generated-for-an-rpc-interface.md).

 

 