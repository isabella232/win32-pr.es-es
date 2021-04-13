---
title: Licencias y IClassFactory2
description: Licencias y IClassFactory2
ms.assetid: 2bead555-8c62-4f48-a4c6-6f0942ec75f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9376d5187588ba14da434161309409bf1d189a8f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421467"
---
# <a name="licensing-and-iclassfactory2"></a>Licencias y IClassFactory2

La interfaz [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) en un objeto de clase proporciona el mecanismo básico de creación de objetos de com. Con **IClassFactory**, un servidor puede controlar la creación de objetos en un equipo. La implementación del método [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) puede permitir o impedir la creación de objetos en función de la existencia de una licencia de equipo. Una licencia de equipo es un fragmento de información independiente de la aplicación que existe en un equipo para indicar que el software se instaló desde un origen válido, como los discos de instalación del proveedor. Si la licencia de la máquina no existe, el servidor puede impedir la creación de objetos. Las licencias de equipo evitan la piratería en los casos en los que un usuario intenta copiar el software de un equipo a otro, ya que la información de licencia no se copia con el software y el equipo que recibe la copia no tiene licencia.

Sin embargo, en un sector del software de componentes, los proveedores necesitan un nivel de control más preciso sobre las licencias. Además del control de licencias por equipo, un proveedor debe permitir que algunos clientes creen un objeto de componente mientras se deniega a otros clientes la misma funcionalidad. Esto requiere que la aplicación cliente obtenga una clave de licencia del componente mientras la aplicación cliente todavía está en desarrollo. La aplicación cliente utiliza la clave de licencia en tiempo de ejecución para crear objetos en una máquina sin licencia.

Por ejemplo, si un proveedor proporciona una biblioteca de controles a los desarrolladores, el desarrollador que compra la biblioteca tendrá una licencia completa de equipo, lo que permite crear los objetos en el equipo de desarrollo. A continuación, el desarrollador puede compilar una aplicación cliente en el equipo con licencia que incorpore uno o varios de los controles. Cuando la aplicación cliente resultante se ejecuta en otro equipo, los controles usados en la aplicación cliente deben crearse en el otro equipo, incluso si ese equipo no posee una licencia de equipo para los controles del proveedor original.

La interfaz [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) proporciona este nivel de control. Para permitir las licencias basadas en claves para cualquier componente determinado, implemente **IClassFactory2** en el objeto de generador de clases para ese componente. **IClassFactory2** se deriva de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), por lo que al implementar **IClassFactory2**, el objeto de generador de clases cumple los requisitos básicos de com.

Para incorporar un componente con licencia en la aplicación cliente, use los métodos siguientes en [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2):

-   El método [**GetLicInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-getlicinfo) rellena una estructura [**LICINFO**](/windows/win32/api/ocidl/ns-ocidl-licinfo) con información que describe el comportamiento de las licencias del generador de clases. Por ejemplo, el generador de clases puede proporcionar claves de licencia para las licencias en tiempo de ejecución si el miembro **fRunTimeKeyAvail** es **true**.
-   El método [**RequestLicKey**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-requestlickey) proporciona una clave de licencia para el componente. Una licencia de equipo debe estar disponible cuando el cliente llama a este método.
-   El método [**CreateInstanceLic**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-createinstancelic) crea una instancia del componente con licencia si el parámetro de clave de licencia (BSTRÂ bstrKey) es válido.

> [!Note]  
> En su información de tipo, un componente utiliza el atributo con licencia para marcar la coclase que admite las licencias a través de [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2).

 

En primer lugar, necesita una herramienta de desarrollo independiente que sea también un cliente del componente con licencia. El propósito de esta herramienta es obtener la clave de licencia en tiempo de ejecución y guardarla en la aplicación cliente. Esta herramienta solo se ejecuta en un equipo que posee una licencia de equipo para el componente. La herramienta llama a los métodos [**GetLicInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-getlicinfo) y [**RequestLicKey**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-requestlickey) para obtener la clave de licencia en tiempo de ejecución y, a continuación, guarda la clave de licencia en la aplicación cliente. Por ejemplo, la herramienta de desarrollo puede crear un archivo de encabezado (. h) que contenga la clave de licencia BSTR y, a continuación, incluiría ese archivo. h en la aplicación cliente.

Para crear una instancia del componente en la aplicación cliente, primero intente crear una instancia del objeto directamente con [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance). Si **CreateInstance** se realiza correctamente, la segunda máquina tiene licencia para el componente y los objetos se pueden crear en. Si se produce un error en **CreateInstance** con la clase de código de retorno \_ E \_ NOTLICENSED, la única manera de crear el objeto es pasar la clave de tiempo de ejecución al método [**CreateInstanceLic**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-createinstancelic) . **CreateInstanceLic** comprueba la clave y crea el objeto si la clave es válida.

De esta manera, una aplicación compilada con componentes (como controles) se puede ejecutar en un equipo que no tiene ninguna otra licencia; solo la aplicación cliente que contiene la licencia en tiempo de ejecución puede crear los objetos de componente en cuestión.

La interfaz [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) admite la flexibilidad en los esquemas de licencias. Por ejemplo, el implementador del servidor puede cifrar las claves de licencia en el componente para mayor seguridad. Los implementadores de servidor también pueden habilitar o deshabilitar niveles de funcionalidad en sus objetos proporcionando diferentes claves de licencia para distintas funciones. Por ejemplo, una clave podría permitir un nivel básico de funcionalidad mientras que otra permite la funcionalidad básica y avanzada, etc.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Responsabilidades del servidor COM](com-server-responsibilities.md)
</dt> </dl>

 

 