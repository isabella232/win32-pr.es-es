---
description: Una vez que la cola se haya confirmado correctamente, deberá actualizar la información del Registro del producto que va a instalar.
ms.assetid: 32161538-c1bd-41a0-bb4f-a32883fe8285
title: Actualización de la información del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 579ef64739bbe063d6fed19234a74b89b86b8b257793a1a26e83fd651256d189
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683055"
---
# <a name="updating-registry-information"></a>Actualización de la información del Registro

Una vez que la cola se haya confirmado correctamente, deberá actualizar la información del Registro del producto que va a instalar. Se recomienda esperar hasta que todas las operaciones de copia de archivos necesarias se hayan completado correctamente antes de modificar la información del Registro.

Una manera de actualizar el Registro es llamar a [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) con las marcas SPINST \_ INIFILES, SPINST REGISTRY o \_ SPINST \_ INI2REG especificadas. Estas marcas se pueden combinar en una llamada a **SetupInstallFromInfSection**.

En el ejemplo siguiente se usa SPINST ALL^SPINST FILES para indicar que la función debe procesar todas las operaciones enumeradas \_ excepto las operaciones de \_ archivo. Puesto que solo las operaciones de ini, registro y archivo se enumeran en la sección Instalación, se trata de un método abreviado para especificar que la función debe procesar todas las operaciones de INI y del Registro. 

En el ejemplo siguiente se muestra cómo instalar información del Registro mediante la **función SetupInstallFromINFSection.**

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

En el ejemplo, *OwnerWindow* es **NULL porque** solo las operaciones de archivo generan cuadros de diálogo y, por tanto, no se necesita una ventana primaria. "MyInf" es el archivo INF que contiene la sección que se va a procesar. El parámetro "MySection" especifica la sección que se va a instalar. Las marcas combinadas, SPINST ALL ^ SPINST FILES, especifican qué operaciones de instalación se deben procesar, en este caso, todas las operaciones excepto \_ \_ las operaciones de archivo. La ruta de acceso raíz de origen se especifica como "A: \\ ".

Puesto que no se está procesando ninguna operación de copia, no se especifican los parámetros *CopyFlags*, *MsgHandler*, *Context*, *DeviceInfoSet* y *DeviceInfoData.*

 

 



