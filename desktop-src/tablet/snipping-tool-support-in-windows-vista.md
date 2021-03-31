---
description: En este tema se describe cómo la aplicación puede especificar qué dirección URL debe obtener la herramienta de recortes de Tablet PC al capturar la aplicación.
ms.assetid: e31e63e8-8f6b-41f7-8bd6-afc5ca32456b
title: Compatibilidad con recortes en Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046dd6c8a97d1dacc20065dc1f741610fec13865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911713"
---
# <a name="snipping-tool-support-in-windows-vista"></a>Compatibilidad con recortes en Windows Vista

En este tema se describe cómo la aplicación puede especificar qué dirección URL debe obtener la herramienta de recortes de Tablet PC al capturar la aplicación.

## <a name="specifying-the-url-via-registry-key"></a>Especificación de la dirección URL mediante la clave del registro

Recortes permite a los usuarios capturar un recorte (captura de pantalla) de cualquier objeto en la pantalla y, a continuación, anotar, guardar o compartir la imagen. Cuando los datos se guardan en formato HTML o cuando se envían a un cliente de correo electrónico que admite HTML en línea, la herramienta recortes puede Agregar una dirección URL al recorte si la aplicación proporciona información sobre cómo obtener la dirección URL.

Recortes obtiene la dirección URL a través de objetos de accesibilidad. Las aplicaciones deben especificar la información necesaria en las siguientes claves del registro:

HKLM \\ software \\ Microsoft \\ Windows \\ TabletPC \\ recortes Tool \\ LinkFingerprints,

Y deben crear una subclave cuyo nombre sea el mismo que el de la clase de ventana de la que se debe obtener el vínculo. El nombre de la clase de ventana debe ser la ventana superior de la aplicación.

HKLM \\ software \\ Microsoft \\ Windows \\ TabletPC \\ recortes Tool \\ LinkFingerprints\\<Window Class Name>

### <a name="window-class-key-details"></a>Detalles de la clave de clase de ventana

En la clave de clase de ventana, se deben establecer los valores adecuados para indicar que la herramienta recortes debe detectar el objeto de accesibilidad correcto.



| VALOR                        | TYPE                  | MÁSCARA            | INFORMACIÓN ALMACENADA                                          |
|------------------------------|-----------------------|-----------------|-------------------------------------------------------------|
| Máscara<br/>              | \_valor DWORD reg<br/> |                 | Indica cuál de los siguientes campos se va a comprobar<br/> |
| Nombre<br/>              | Registro \_ SZ<br/>    | 0x02<br/> | Nombre de accesibilidad<br/>                               |
| Descripción<br/>       | Registro \_ SZ<br/>    | 0x04<br/> | Descripción de accesibilidad<br/>                        |
| Role<br/>              | \_valor DWORD reg<br/> | 0x08<br/> | Rol de accesibilidad<br/>                               |
| ParentName<br/>        | Registro \_ SZ<br/>    | 0x10<br/> | Nombre de accesibilidad del elemento primario<br/>                     |
| ParentValue<br/>       | Registro \_ SZ<br/>    | 0x20<br/> | Valor de accesibilidad de primario<br/>                    |
| ParentRole<br/>        | \_valor DWORD reg<br/> | 0x40<br/> | Rol de accesibilidad del elemento primario<br/>                     |
| ParentDescription<br/> | Registro \_ SZ<br/>    | 0x80<br/> | Descripción de accesibilidad de la principal<br/>              |



 

Además, si se establece el valor de bit de máscara 0x1, la dirección URL debe tomarse del nombre de accesibilidad; de lo contrario, la dirección URL debe tomarse del valor de accesibilidad.

Si la aplicación utiliza cadenas localizadas para los valores de REG \_ SZ anteriores, se debe proporcionar la cadena como una cadena indirecta con el siguiente formato:

@filename, recurso

La cadena se extrae del archivo denominado, utilizando el valor de recurso como localizador. Si el valor del recurso es cero o mayor, el número se convierte en el índice de la cadena en el archivo binario. Si el número es negativo, se convierte en un identificador de recursos (ID.).

> [!Note]  
> Las constantes de rol se pueden encontrar en oleacc. h en el Windows SDK. Los valores del registro descritos son específicos de Windows Vista.

 

 

 




