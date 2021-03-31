---
title: Programar ADSI con Java/COM
description: Con la máquina virtual de Microsoft para Java (máquina virtual de Microsoft) y el compilador de Microsoft Java, tiene acceso a todas las características de ADSI expuestas a través de los componentes COM ADSI, desde una aplicación Java/COM.
ms.assetid: eda516b6-0f89-464f-a9d2-9bb4ca70fda5
ms.tgt_platform: multiple
keywords:
- Programar ADSI con Java/COM AD
- ADSI ADSI, usar, programación con Java/COM para
- ADSI ADSI, código de ejemplo Java
- ADSI ADSI, código de ejemplo Java, enlazar a un objeto ADSI e invocar métodos en ese objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6899804208f9899823f266bc941bcf3c2dec372
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903035"
---
# <a name="programming-adsi-with-javacom"></a>Programar ADSI con Java/COM

Con la máquina virtual de Microsoft para Java (máquina virtual de Microsoft) y el compilador de Microsoft Java, tiene acceso a todas las características de ADSI expuestas a través de los componentes COM ADSI, desde una aplicación Java/COM. En el siguiente ejemplo de código de Java se muestran los elementos necesarios para enlazar a un objeto ADSI e invocar métodos en ese objeto. Los métodos de objeto y las funciones de la API ADSI necesarios se exponen a través de Activeds.dll.


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



El argumento de la primera instrucción **Import** hace referencia a las clases contenedoras de Java empaquetadas en Activeds.dll. Use Visual J++ para crear las clases contenedoras e incluirlas en el proyecto siguiendo el procedimiento que se indica a continuación.

**Para crear clases contenedoras e incluirlas en el proyecto**

1.  En un proyecto de Visual J++, seleccione **Agregar contenedor com...** en el menú **proyecto** .
2.  Seleccione "biblioteca de tipos Active DS" en los **componentes instalados:** en el cuadro de diálogo contenedores com. Si la biblioteca de tipos no se muestra en el cuadro de lista, haga clic en el botón **examinar...** , desplácese hasta el directorio donde se almacena activeds. tlb y, a continuación, seleccione la biblioteca de tipos.

Visual J++ crea el paquete activeds para las clases contenedoras de Java e incluye el paquete en la ruta de acceso predeterminada del proyecto. Para obtener más información, vea el paquete activeds en el panel de **exploración del proyecto** en la ventana de Visual J++.

Para obtener un objeto ADSI que no se pueda crear, use una de las funciones de la API ADSI expuestas, por ejemplo, [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) o [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), que también se empaquetan en Activeds.dll. Microsoft J/Direct proporciona acceso a estas y otras API nativas. Esto se muestra en las dos últimas líneas del ejemplo de código anterior.

Al compilar, asegúrese de que la extensión de idioma de Microsoft está habilitada. Para ello, seleccione **<project> propiedades...** en el menú **proyecto** de la ventana proyecto de Visual J++. A continuación, haga clic en la pestaña **compilar** en el cuadro de diálogo **<project> propiedades** . Desactive la casilla **deshabilitar extensiones de lenguaje de Microsoft** . Si compila desde la línea de comandos, use el modificador "/x-", por ejemplo:

**JVC/x-SimpleADSI. Java**

Por último, para que la máquina virtual cargue el componente COM, la biblioteca de vínculos dinámicos (DLL) debe estar visible en la ruta de acceso del sistema. Si se devuelve un error "Java. lang. UnsatisfiedLinkError", establezca la ruta de acceso para incluir la ruta de acceso que contiene el archivo DLL necesario. Por ejemplo, si se ha instalado Activeds.dll en c: \\ ADSI \\ lib, emita el siguiente comando desde la línea de comandos:

**establecer ruta de acceso =% PATH%; c: \\ ADSI \\ lib**

 

 




