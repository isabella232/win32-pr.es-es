---
description: En este tema se describe cómo la aplicación puede especificar qué dirección URL debe Herramienta Recortes tablet PC al capturar la aplicación.
ms.assetid: e31e63e8-8f6b-41f7-8bd6-afc5ca32456b
title: Herramienta Recortes compatibilidad con Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb2c24901524500df97461f3b3acf88d9a51f73cc24134955c1df866a457a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966774"
---
# <a name="snipping-tool-support-in-windows-vista"></a>Herramienta Recortes compatibilidad con Windows Vista

En este tema se describe cómo la aplicación puede especificar qué dirección URL debe Herramienta Recortes tablet PC al capturar la aplicación.

## <a name="specifying-the-url-via-registry-key"></a>Especificar la dirección URL a través de la clave del Registro

Herramienta Recortes permite a los usuarios capturar un snip (captura de pantalla) de cualquier objeto de la pantalla y, a continuación, anotar, guardar o compartir la imagen. Cuando los datos se guardan en formato HTML o cuando se envían a un cliente de correo electrónico que admite HTML en línea, Herramienta Recortes puede agregar una dirección URL a snip si la aplicación proporciona información sobre cómo obtener la dirección URL.

Herramienta Recortes obtiene la dirección URL a través de objetos de accesibilidad. Las aplicaciones deben especificar la información necesaria en las siguientes claves del Registro:

HKLM \\ Software Microsoft Windows \\ \\ \\ TabletPC Herramienta Recortes \\ \\ LinkFiprintprints,

Y debe crear una subclave cuyo nombre sea el mismo que la clase de ventana de la que se debe obtener el vínculo. El nombre de clase de ventana debe ser la ventana superior de la aplicación.

HKLM \\ Software Microsoft Windows \\ \\ \\ TabletPC Herramienta Recortes \\ \\ LinkFiprintprints\\<Window Class Name>

### <a name="window-class-key-details"></a>Detalles de clave de clase de ventana

En la clave de clase de ventana, se deben establecer los valores adecuados para indicar Herramienta Recortes debe detectar el objeto de accesibilidad correcto.



| VALOR                        | TYPE                  | Máscara            | INFORMACIÓN ALMACENADA                                          |
|------------------------------|-----------------------|-----------------|-------------------------------------------------------------|
| Máscara<br/>              | REG \_ DWORD<br/> |                 | Indica cuál de los siguientes campos se va a comprobar<br/> |
| Nombre<br/>              | REG \_ SZ<br/>    | 0x02<br/> | Nombre de accesibilidad<br/>                               |
| Descripción<br/>       | REG \_ SZ<br/>    | 0x04<br/> | Descripción de accesibilidad<br/>                        |
| Rol<br/>              | REG \_ DWORD<br/> | 0x08<br/> | Rol de accesibilidad<br/>                               |
| ParentName<br/>        | REG \_ SZ<br/>    | 0x10<br/> | Nombre de accesibilidad del elemento primario<br/>                     |
| ParentValue<br/>       | REG \_ SZ<br/>    | 0x20<br/> | Valor de accesibilidad del elemento primario<br/>                    |
| ParentRole<br/>        | REG \_ DWORD<br/> | 0x40<br/> | Rol de accesibilidad del elemento primario<br/>                     |
| ParentDescription<br/> | REG \_ SZ<br/>    | 0x80<br/> | Descripción de accesibilidad del elemento primario<br/>              |



 

Además, si se establece el valor de bits 0x1 máscara, la dirección URL debe tomarse del nombre de accesibilidad; De lo contrario, la dirección URL debe tomarse del valor de accesibilidad.

Si la aplicación usa cadenas localizadas para los valores REG SZ anteriores, la cadena debe proporcionarse como una cadena indirecta \_ con el formato siguiente:

@filenameRecursos

La cadena se extrae del archivo denominado , utilizando el valor de recurso como localizador. Si el valor del recurso es cero o mayor, el número se convierte en el índice de la cadena en el archivo binario. Si el número es negativo, se convierte en un identificador de recurso (ID).

> [!Note]  
> Las constantes de rol se pueden encontrar en oleacc.h en Windows SDK. Los valores del Registro descritos son específicos de Windows Vista.

 

 

 




