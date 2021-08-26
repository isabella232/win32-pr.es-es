---
description: PROPERTYKEYs y GUID en Windows dispositivos portátiles
ms.assetid: 3f9e9f29-37dd-47b0-997e-de81966efce2
title: PROPERTYKEYs y GUID en Windows dispositivos portátiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80100b043383074f58bc27fe8e9782c4fd6d2e4f3841a28f37035f39d23cc7c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054875"
---
# <a name="propertykeys-and-guids-in-windows-portable-devices"></a>PROPERTYKEYs y GUID en Windows dispositivos portátiles

Una propiedad o comando se identifica mediante una estructura PROPERTYKEY. Una estructura PROPERTYKEY se forma de dos partes: un GUID (el miembro fmtid) y un DWORD (el miembro pid). La parte GUID se usa para indicar la categoría a la que pertenece la propiedad o el comando (es decir, las propiedades relacionadas pertenecen a la misma categoría y los comandos relacionados pertenecen a la misma categoría; por lo tanto, tendrán el mismo fmtid). La parte DWORD indica la propiedad o el identificador de comando y se usa para distinguir las propiedades o comandos individuales dentro de una propiedad o categoría de comandos (es decir, los valores pid de las propiedades o comandos de la misma categoría serán diferentes).

En la sección de referencia de este documento se describen todos los valores PROPERTYKEY definidos por WPD; estos valores corresponden a comandos, propiedades y recursos. Si crea un valor PROPERTYKEY personalizado, debe definir una nueva **categoría GUID;** no reutilice los valores **GUID de** WPD o corre el riesgo de conflicto con propertyKEYs existentes y futuras especificadas por WPD.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción a la aplicación**](application-overview.md)
</dt> <dt>

[**Comandos**](commands.md)
</dt> <dt>

[**GUID de formato de objeto**](object-format-guids.md)
</dt> <dt>

[**Propiedades y atributos**](properties-and-attributes.md)
</dt> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



