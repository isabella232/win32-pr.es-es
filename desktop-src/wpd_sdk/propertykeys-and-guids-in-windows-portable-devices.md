---
description: PROPERTYKEYs y GUID en Windows dispositivos portátiles
ms.assetid: 3f9e9f29-37dd-47b0-997e-de81966efce2
title: PROPERTYKEYs y GUID en Windows dispositivos portátiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28cbe76b76eda04852cd1afcbb11b85b0a185d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251355"
---
# <a name="propertykeys-and-guids-in-windows-portable-devices"></a>PROPERTYKEYs y GUID en Windows dispositivos portátiles

Una propiedad o comando se identifica mediante una estructura PROPERTYKEY. Una estructura PROPERTYKEY se forma de dos partes: un GUID (el miembro fmtid) y un DWORD (el miembro pid). La parte GUID se usa para indicar la categoría a la que pertenece la propiedad o el comando (es decir, las propiedades relacionadas pertenecen a la misma categoría y los comandos relacionados pertenecen a la misma categoría; por lo tanto, tendrán el mismo fmtid). La parte DWORD indica la propiedad o el identificador de comando, y se usa para distinguir las propiedades o comandos individuales dentro de una propiedad o categoría de comando (es decir, los valores pid de las propiedades o comandos de la misma categoría serán diferentes).

En la sección de referencia de este documento se describen todos los valores PROPERTYKEY definidos por WPD; estos valores corresponden a comandos, propiedades y recursos. Si crea un valor PROPERTYKEY personalizado, debe definir una nueva **categoría GUID;** no reutilice los valores **GUID de** WPD o corre el riesgo de que entre en conflicto con propertyKEYs existentes y futuros especificados por WPD.

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

 

 



