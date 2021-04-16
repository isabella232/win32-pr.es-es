---
description: El proceso de codificación es el inverso del proceso de descodificación descrito en descodificar una estructura de información de certificado \_ .
ms.assetid: 5d3311e5-a2fb-46f7-aa76-f232b39b34fd
title: Codificar una estructura de CERT_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645a1d3054546a7b11c57d4f515dc7d3e26b5fe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669815"
---
# <a name="encoding-a-cert_info-structure"></a>Codificar una estructura de información de certificado \_

El proceso de codificación es el inverso del proceso de descodificación descrito en [descodificar una \_ estructura de información de certificado](decoding-a-cert-info-structure.md). Por ejemplo, el siguiente procedimiento agregaría un **emisor** codificado a una estructura de [**\_ información de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) . Vea también la ilustración que sigue al procedimiento.

**Para agregar un emisor codificado a una estructura de información de certificado \_**

1.  Cree una cadena que contenga el nombre del emisor que se va a usar.
2.  Cree una matriz de estructuras [**CERT \_ RDN \_ ATTR**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) , que se inicializará para contener la información adecuada sobre la cadena del nombre del emisor que acaba de crear.
3.  Cree una matriz de [**estructuras \_ RDN de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) , una de las cuales tiene la información sobre la matriz de estructuras de [**CERT \_ RDN \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) que se acaba de inicializar.
4.  Cree una estructura de [**\_ \_ información de nombre de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) que tenga un puntero a la matriz de estructuras de [**CERT \_ RDN**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) que acaba de crear.
5.  Llame a [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) para obtener el tamaño del BLOB codificado de salida, pasándole la dirección de la estructura de [**\_ \_ información del nombre de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) que acaba de crear.
6.  Asigne memoria para el BLOB codificado de salida.
7.  Vuelva a llamar a [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) , pasándole la misma información, pero ahora pásele la dirección de la memoria que acaba de asignar.
8.  Establezca el miembro **issuer. cbData** de la estructura de [**\_ información de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) en el tamaño devuelto en el paso 5 y el miembro **issuer. pbData** en la dirección obtenida en el paso 6. El BLOB de **emisor** codificado ahora reside allí.

![Agregar un emisor codificado a una estructura de información de certificado \-](images/encflow.png)

Para inicializar y codificar parte de la información de la extensión del certificado, use el procedimiento siguiente. Vea también la ilustración que sigue al procedimiento.

**Para agregar información de extensión codificada a una estructura de información de certificado \_**

1.  Crear e inicializar una estructura de información de la extensión: en este ejemplo, es una estructura de información de [**\_ \_ restricciones \_ básicas de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info) .
2.  Llame a [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject), pasándole la dirección de la estructura que acaba de crear, para obtener el tamaño del BLOB codificado de salida.
3.  Asigne memoria para el BLOB codificado de salida.
4.  Llame de nuevo a [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) , pasando la misma información, excepto que ahora pasa la dirección de la memoria asignada.
5.  Cree una matriz de estructuras de [**\_ extensión de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) .
6.  Inicialice una de las estructuras de [**\_ extensión de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) para **que pszObjId** sea la cadena adecuada para los datos contenidos en el **valor** y ese **valor** contenga el BLOB de datos cifrados que se ha generado desde la llamada a [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject).
7.  Inicialice el miembro **rgExtension** de la estructura de [**\_ información de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) para que apunte a la matriz de estructuras de [**\_ extensión de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) .

![agregar información de extensión codificada a una estructura de información de certificado \-](images/xtenflow.png)

 

 



