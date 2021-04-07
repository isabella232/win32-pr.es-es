---
description: Una vez confirmada correctamente la cola, deberá actualizar la información del registro para el producto que está instalando.
ms.assetid: 32161538-c1bd-41a0-bb4f-a32883fe8285
title: Actualizando información del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aa6a77f231f3a4fe754b589e3f20ed67e78e548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002655"
---
# <a name="updating-registry-information"></a>Actualizando información del registro

Una vez confirmada correctamente la cola, deberá actualizar la información del registro para el producto que está instalando. Se recomienda que espere hasta que todas las operaciones de copia de archivos necesarias se hayan completado correctamente antes de modificar la información del registro.

Una manera de actualizar el registro es llamar a [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) con el INIFILES de giro \_ , el registro más o las marcas de INI2REG de \_ giro \_ especificadas. Estas marcas se pueden combinar en una llamada a **SetupInstallFromInfSection**.

En el ejemplo siguiente se usan más de% \_ archivos de bucle \_ para indicar que la función debe procesar todas las operaciones de la lista excepto las operaciones de archivo. Dado que solo las operaciones INI, Registry y file se enumeran en la sección **install** , se trata de un método abreviado para especificar la función que debe procesar todas las operaciones ini y del registro.

En el ejemplo siguiente se muestra cómo instalar la información del registro mediante la función **SetupInstallFromINFSection** .

``` syntax
Test = SetupInstallFromINFSection (
     NULL,                     //Window to own any dialog boxes
                               //created 
     MyInf,                    //INF file containing the section 
     MySection,                //the section to install
     SPINST_ALL ^ SPINST_FILES,//which installation operations 
                               //to process
     NULL,                     //the relative root key
     NULL,                     //the source root path
     0,                        //copy style
     NULL,                     //Message handler routine
     NULL,                     //Context
     NULL,                     //Device info set
     NULL                      //device info data
);
```

En el ejemplo, *OwnerWindow* es **null** porque solo las operaciones de archivo generan cuadros de diálogo y, por lo tanto, no se necesita una ventana primaria. "MyInf" es el archivo INF que contiene la sección que se va a procesar. El parámetro, "nosection", especifica la sección que se va a instalar. Las marcas combinadas, \_ los más de los ^ \_ archivos de bucle, especifican las operaciones de instalación que se van a procesar, en este caso, todas las operaciones excepto las operaciones de archivo. La ruta de acceso raíz de origen se especifica como "A: \\ ".

Dado que no se está procesando ninguna operación de copia, no se especifican los parámetros *CopyFlags*, *MsgHandler*, *Context*, *DeviceInfoSet* y *DeviceInfoData* .

 

 



