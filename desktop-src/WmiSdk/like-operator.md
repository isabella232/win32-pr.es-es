---
description: El operador LIKE determina si una cadena de caracteres coincide o no con un patrón especificado.
ms.assetid: 6cafe696-891d-4b17-8802-4b872f76fc78
ms.tgt_platform: multiple
title: Operador LIKE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9091f44dd131d5d2c30d2d46aa4fc109dcdf02b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249357"
---
# <a name="like-operator"></a>Operador LIKE

El operador LIKE determina si una cadena de caracteres coincide o no con un patrón especificado. El patrón especificado puede contener exactamente los caracteres que deben coincidir o puede contener meta caracteres. De hecho, el operador LIKE coincide con subcadenas mediante los caracteres comodín de la tabla siguiente.



| Carácter       | Descripción                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[ \]           | Cualquier carácter dentro del intervalo especificado ( \[ a-f \] ) o set ( \[ abcdef \] ).                                                                                                                 |
| ^               | Cualquier carácter que no se encuentra dentro del intervalo ( \[ ^a-f \] ) o establecido ( \[ ^abcdef \] ).                                                                                                                     |
| %               | Cualquier cadena de 0 (cero) o más caracteres. En el ejemplo siguiente se encuentran todas las instancias en las que "Win" se encuentra en cualquier lugar del nombre de clase: `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"` |
| \_ (subrayado) | Cualquier carácter. Cualquier carácter de subrayado literal utilizado en la cadena de consulta debe incluirse entre \[ \] corchetes.                                                             |



 

Por ejemplo, el siguiente código de Power Shell recupera todas las instancias de la clase **\_ operatingSystem win32** cuya propiedad **Name** comienza por **FirstName**:

`Get-WmiObject win32_computerSystem -filter "Name LIKE 'FirstName%'"`

Dado que el carácter de subrayado es un carácter meta, si el destino de la consulta tiene un carácter de subrayado, los caracteres de \[ \] escape "" deben rodearse. Por ejemplo, puede consultar todas las clases que tienen un carácter de subrayado doble en el nombre.

Para buscar todas las clases con un carácter de subrayado doble en el nombre, debe usar caracteres de escape con caracteres de subrayado \[ \] (corchetes), por ejemplo:

`SELECT * FROM meta_class WHERE __CLASS LIKE "%[_][_]%"`

Puede negar una instrucción LIKE mediante NOT; Para ello, asegúrese de colocar NOT directamente delante del nombre del campo. Por ejemplo:

`  Get-WmiObject -computerName "." -query 'Select * FROM Win32_Printer WHERE Local="TRUE"      AND Network ="False" AND DriverName LIKE "%HP%"      AND NOT PortName LIKE "%10.%" AND NOT PortName LIKE "%\\%"'`

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Operadores WQL](wql-operators.md)
</dt> </dl>

 

 



