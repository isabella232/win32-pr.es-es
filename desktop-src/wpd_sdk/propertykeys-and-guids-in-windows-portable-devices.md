---
description: PROPERTYKEYs y GUID en dispositivos portátiles de Windows
ms.assetid: 3f9e9f29-37dd-47b0-997e-de81966efce2
title: PROPERTYKEYs y GUID en dispositivos portátiles de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28cbe76b76eda04852cd1afcbb11b85b0a185d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911125"
---
# <a name="propertykeys-and-guids-in-windows-portable-devices"></a>PROPERTYKEYs y GUID en dispositivos portátiles de Windows

Una propiedad o un comando se identifica mediante una estructura PROPERTYKEY. Una estructura PROPERTYKEY se compone de dos partes: un GUID (el miembro fmtid) y un valor DWORD (el miembro PID). La parte del GUID se usa para indicar la categoría a la que pertenece la propiedad o el comando (es decir, las propiedades relacionadas pertenecen a la misma categoría y los comandos relacionados pertenecen a la misma categoría; por lo tanto, tendrán el mismo fmtid). La parte DWORD indica el identificador de la propiedad o del comando, y se usa para distinguir las propiedades o los comandos individuales dentro de una categoría de propiedad o de comando (es decir, los valores de PID para propiedades o comandos de la misma categoría serán diferentes).

La sección de referencia de este documento describe todos los valores de PROPERTYKEY definidos por WPD; Estos valores corresponden a comandos, propiedades y recursos. Si crea un valor de PROPERTYKEY personalizado, debe definir una nueva categoría de **GUID** ; No reutilice los valores de **GUID** de WPD o se arriesga a que se produzcan conflictos con los PROPERTYKEYs existentes y futuros especificados por WPD.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información general de la aplicación**](application-overview.md)
</dt> <dt>

[**Comandos:**](commands.md)
</dt> <dt>

[**GUID de formato de objeto**](object-format-guids.md)
</dt> <dt>

[**Propiedades y atributos**](properties-and-attributes.md)
</dt> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



