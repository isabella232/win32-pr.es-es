---
description: Si utiliza varios reconocedores, puede usar la colección Recognizers para enumerar los reconocedores disponibles y permitir que un usuario seleccione entre ellos.
ms.assetid: 1b89def0-3491-42da-9138-5280002e447a
title: Usar la colección Recognizers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d38625b3c6d4b8ed2475393ba45ae97b5bdc47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659799"
---
# <a name="using-the-recognizers-collection"></a>Usar la colección Recognizers

Si utiliza varios reconocedores, puede usar la colección [**Recognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) para enumerar los reconocedores disponibles y permitir que un usuario seleccione entre ellos. Una colección de **reconocedores** comprueba los reconocedores instalados, consulta los atributos de los objetos de [**reconocedor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) y almacena los resultados. Las aplicaciones pueden usar la colección **reconocedores** para mostrar una lista de los reconocedores disponibles sin cargar cada dll del reconocedor.

> [!Note]  
> La colección [**Recognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) utiliza el registro del sistema para buscar reconocedores de Microsoft y reconocedores de terceros.

 

En la tabla siguiente se muestran los valores de los identificadores de idioma que admite cada reconocedor de Microsoft.

> [!Note]  
> No hay identificadores de idioma asociados al reconocedor de gestos de Microsoft.

 



| Nombre del reconocedor                                                      | Identificador de idioma principal, identificador de subidioma (compatible con el orden)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reconocedor de gestos de Microsoft<br/>                              | None<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Reconocedor de escritura a mano en inglés (Reino Unido) de Microsoft<br/> | LANG \_ Inglés, sublang \_ Inglés ( \_ Reino Unido)<br/> LANG \_ Inglés, sublang \_ Inglés \_ Eire<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Reconocedor de escritura a mano en Inglés de Microsoft (Estados Unidos)<br/>  | LANG \_ Inglés, sublang \_ Inglés ( \_ EE. UU.)<br/> LANG \_ Inglés, sublang \_ Inglés ( \_ Australia)<br/> LANG \_ Inglés, sublang \_ Inglés \_ Belice<br/> LANG \_ Inglés, sublang \_ Inglés \_<br/> LANG \_ Inglés, sublang \_ Inglés del \_ Caribe<br/> LANG \_ Inglés, sublang \_ Inglés \_ Jamaica<br/> LANG \_ Inglés, sublang \_ Inglés \_ NZ<br/> LANG \_ Inglés, sublang \_ Inglés \_ Filipinas<br/> LANG \_ Inglés, sublang \_ Inglés ( \_ Sudáfrica) \_<br/> LANG \_ Inglés, sublang \_ Inglés \_ Trinidad<br/> LANG \_ Inglés, sublang \_ Inglés \_ Zimbabue<br/> LANG \_ Inglés, sublang \_ neutro<br/> |
| Reconocedor de escritura a mano francés de Microsoft<br/>                   | LANG \_ Francés, sublang \_ Francés<br/> LANG \_ Francés, sublang \_ Francés \_ belga<br/> LANG \_ Francés, sublang \_ Francés \_ canadiense<br/> LANG \_ Francés, sublang \_ Francés \_ Luxembourg<br/> LANG \_ Francés, sublang \_ Francés \_ Mónaco<br/> LANG \_ Francés, sublang \_ Francés \_ suizo<br/> LANG \_ Francés, sublang \_ neutro<br/>                                                                                                                                                                                                                                                                                     |
| Reconocedor de escritura a mano alemán de Microsoft<br/>                   | LANG \_ alemán, sublang \_ alemán<br/> LANG \_ alemán, sublang \_ Alemán \_ austriaco<br/> LANG \_ alemán, sublang \_ Alemán \_ Liechtenstein<br/> LANG \_ alemán, sublang \_ Alemán \_ Luxemburgo<br/> LANG \_ alemán, sublang \_ Alemán \_ suizo<br/> LANG \_ alemán, sublang \_ neutro<br/>                                                                                                                                                                                                                                                                                                                                |
| Reconocedor de escritura a mano Español de Microsoft<br/>                  | LANG \_ Español, sublang \_ Español<br/> LANG \_ Español, sublang \_ neutro<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Reconocedor de escritura a mano japonés de Microsoft<br/>                 | LANG \_ japonés, sublang \_ neutro<br/> LANG \_ japonés, sublang \_ predeterminado<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Reconocedor de escritura a mano de Microsoft Coreano<br/>                   | LANG \_ Coreano, sublang \_ neutro<br/> LANG \_ Coreano, valor predeterminado de SUBlang \_<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Reconocedor de escritura a mano en Chino (simplificado) de Microsoft<br/>     | LANG \_ chino, sublang \_ chino \_ simplificado<br/> LANG \_ chino, sublang \_ chino de \_ Singapur<br/> LANG \_ chino, sublang \_ neutro<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Reconocedor de escritura a mano en Chino (tradicional) de Microsoft<br/>    | LANG \_ chino, sublang \_ chino \_ tradicional<br/> LANG \_ chino, sublang \_ chino \_ Hong Kong<br/> LANG \_ chino, sublang \_ chino \_ Macao<br/> LANG \_ chino, sublang \_ neutro<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

Para obtener más información sobre los identificadores de idioma, vea [constantes y cadenas de identificador de idioma](../intl/language-identifier-constants-and-strings.md).

 

 
