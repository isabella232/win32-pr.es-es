---
description: El proceso de codificación es el inverso del proceso de codificación descrito en Decoding a CERT INFO Structure (Decoding a CERT \_ INFO Structure).
ms.assetid: 5d3311e5-a2fb-46f7-aa76-f232b39b34fd
title: Codificación de una CERT_INFO estructura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645a1d3054546a7b11c57d4f515dc7d3e26b5fe0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476450"
---
# <a name="encoding-a-cert_info-structure"></a>Codificación de una estructura \_ CERT INFO

El proceso de codificación es el inverso del proceso de codificación descrito en [Decoding a CERT \_ INFO Structure](decoding-a-cert-info-structure.md). Por ejemplo, el siguiente procedimiento agregaría un emisor **codificado** a una estructura [**CERT \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) Consulte también la ilustración que sigue al procedimiento.

**Para agregar un emisor codificado a una estructura CERT \_ INFO**

1.  Cree una cadena que contenga el nombre del emisor que se va a usar.
2.  Cree una matriz de [**estructuras \_ CERT RDN \_ ATTR,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) que se inicializarán para contener la información adecuada sobre la cadena de nombre del emisor que acaba de crear.
3.  Cree una matriz de [**estructuras \_ DE RDN**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) de CERT, una de las cuales tiene la información sobre la matriz de estructuras [**DE \_ \_ ATTR de CERT RDN**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) que se acaba de inicializar.
4.  Cree una [**estructura CERT \_ NAME \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) que tenga un puntero a la matriz de estructuras [**DE \_ RDN**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) de CERT que acaba de crear.
5.  Llame [**a CryptEncodeObject para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) obtener el tamaño del blob codificado de salida y pasarle la dirección de la estructura CERT NAME [**\_ \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) que acaba de crear.
6.  Asigne memoria para el blob codificado en la salida.
7.  Vuelva a llamar a [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) y pase la misma información, pero ahora pase la dirección de la memoria que acaba de asignar.
8.  Establezca el **miembro Issuer.cbData** de la estructura [**CERT \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) en el tamaño devuelto en el paso 5 y el miembro **Issuer.pbData** en la dirección obtenida en el paso 6. El blob **del emisor codificado** ahora reside allí.

![agregar un emisor codificado a una estructura de \- información de certificado](images/encflow.png)

Para inicializar y codificar alguna información de extensión de certificado, use el procedimiento siguiente. Consulte también la ilustración que sigue al procedimiento.

**Para agregar información de extensión codificada a una estructura CERT \_ INFO**

1.  Cree e inicialice una estructura de información de extensión; en este ejemplo, es una [**estructura CERT \_ BASIC \_ CONSTRAINTS \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info)
2.  Llame [**a CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)y pase la dirección de la estructura que acaba de crear para obtener el tamaño del blob codificado de salida.
3.  Asigne memoria para el blob codificado en la salida.
4.  Vuelva [**a llamar a CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) y pase la misma información, excepto que pase ahora la dirección de la memoria asignada.
5.  Cree una matriz de [**estructuras \_ DE EXTENSIÓN CERT.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension)
6.  Inicialice una de las estructuras [**\_ DE EXTENSIÓN CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) para que **pszObjId** sea la cadena adecuada para los datos contenidos en **Value** y que **Value** contenga el BLOB de datos cifrados que se ha devuelto de la llamada a [**CryptEncodeObject.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)
7.  Inicialice el **miembro rgExtension** de la [**estructura CERT \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) para que apunte a la matriz de estructuras [**DE EXTENSIÓN \_ CERT.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension)

![agregar información de extensión codificada a una estructura de \- información de certificado](images/xtenflow.png)

 

 



