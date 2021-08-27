---
title: Programación de ADSI con Java/COM
description: Con la máquina virtual de Microsoft para Java (vm de Microsoft) y el compilador de Microsoft Java, tiene acceso a todas las características adsi expuestas a través de cualquier componente COM adsi, desde una aplicación Java/COM.
ms.assetid: eda516b6-0f89-464f-a9d2-9bb4ca70fda5
ms.tgt_platform: multiple
keywords:
- Programación de ADSI con Java/COM AD
- ADSI ADSI , mediante, programación java/COM para
- ADSI ADSI, código de ejemplo java
- ADSI ADSI, código de ejemplo Java, enlace a un objeto ADSI e invocación de métodos en ese objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec873822d27a7b5fcf95aad7c31a8978552eb88
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880295"
---
# <a name="programming-adsi-with-javacom"></a>Programación de ADSI con Java/COM

Con la máquina virtual de Microsoft para Java (vm de Microsoft) y el compilador de Microsoft Java, tiene acceso a todas las características adsi expuestas a través de cualquier componente COM adsi, desde una aplicación Java/COM. En el ejemplo de código de Java siguiente se muestran los elementos necesarios para enlazar a un objeto ADSI e invocar métodos en ese objeto. Las funciones de API ADSI y los métodos de objeto necesarios se exponen a través de Activeds.dll.


```C++
import activeds.*;       // ADSI COM Wrapper classes
import com.ms.com.*;     // to use _Guid data type in COM.

public Class SimpleADSI 
{
    IADs obj;
    String path = "WinNT://domain/machine,computer";
    _Guid riid = IADs.iid;
    public static void main(String args[]) 
    {
        try 
        {
            obj = (IADs)ADsGetObject(path, riid);
            System.out.println( "Object name:  " + obj.getName() );
            System.out.println( "      class:  " + obj.getSchema() );
            System.out.println( "    ADsPath:  " + obj.getADsPath() );
            System.out.println( "     parent:  " + obj.getParent() );
        }
        catch (Exception e) 
        {
            System.out.println( "SimpleADSI Error: " + e.toString() );
        }
    }

    /** @dll.import("activeds", ole) */
    private static native IUnknown ADsGetObject(String path, _Guid riid);
}
```



El argumento de la primera **instrucción import** hace referencia a las clases de contenedor de Java empaquetadas en Activeds.dll. Use Visual J++ para crear las clases contenedoras e incluirlas en el proyecto, siguiendo el procedimiento siguiente.

**Para crear clases contenedoras e incluirlas en el proyecto**

1.  En un proyecto de Visual J++, seleccione **Agregar contenedor com...** en el **Project.**
2.  Seleccione "Active DS Type Library" (Biblioteca de tipos DS activos) en el cuadro de diálogo **Componentes instalados:** en el cuadro de diálogo Contenedores COM. Si la biblioteca de tipos no se  muestra en el cuadro de lista, haga clic en el botón Examinar..., vaya al directorio donde se almacena Activeds.tlb y, a continuación, seleccione la biblioteca de tipos.

Visual J++ crea el paquete activeds para las clases de contenedor de Java e incluye el paquete en la ruta de acceso predeterminada del proyecto. Para obtener más información, vea el paquete activeds en el **Project explorar** en la ventana de Visual J++.

Para obtener un objeto ADSI que no se puede crear de forma cocreada, use una de las funciones de API ADSI expuestas, por ejemplo, [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) o [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), que también se empaquetan en Activeds.dll. Microsoft J/Direct proporciona acceso a estas y otras API nativas. Esto se ilustra en las dos últimas líneas del ejemplo de código anterior.

Al compilar, asegúrese de que la extensión de lenguaje de Microsoft está habilitada. Para ello, seleccione **&lt; Propiedades del &gt; proyecto...** en el **Project** en la ventana del proyecto de Visual J++. A continuación, haga clic **en la pestaña** Compilar del cuadro de diálogo Propiedades **&lt; &gt; del** proyecto. Desactive la **casilla Deshabilitar extensiones de lenguaje de Microsoft.** Si se compila desde la línea de comandos, use el modificador "/x-", por ejemplo:

**y /x- SimpleADSI.java**

Por último, para que la máquina virtual cargue el componente COM, la biblioteca de vínculos dinámicos (DLL) debe estar visible en la ruta de acceso del sistema. Si se devuelve un error "java.lang.UnsatisfiedLinkError", establezca PATH para incluir la ruta de acceso que contiene el archivo DLL necesario. Por ejemplo, si Activeds.dll se ha instalado en c: adsi lib, emita el siguiente comando \\ desde la línea de \\ comandos:

**set PATH = %PATH%; c: \\ adsi \\ lib**

 

 




