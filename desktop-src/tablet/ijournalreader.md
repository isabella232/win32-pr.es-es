---
description: Proporciona acceso de lectura a un Windows journal, devolviendo una secuencia que contiene una versión XML del contenido del archivo.
ms.assetid: e4e19f69-6377-4f06-856d-7f9b453e7656
title: Interfaz IJournalReader (Journal.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IJournalReader
api_type:
- COM
api_location:
- Journal.dll
ms.openlocfilehash: ff0151432e38a3e611e09efe2d5192eefb8c1d3e6cb0e79296e992b728c5a16a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590323"
---
# <a name="ijournalreader-interface"></a>Interfaz IJournalReader

Proporciona acceso de lectura a un Windows journal, devolviendo una secuencia que contiene una versión XML del contenido del archivo.

> [!Note]  
> El componente Lector de diario no puede leer Windows de diario creados por máquinas que ejecutan Windows 7 o posterior. La interfaz IJournalReader debe considerarse en desuso o obsoleta y no debe usarse.

 

## <a name="members"></a>Miembros

La **interfaz IJournalReader** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IJournalReader** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IJournalReader** tiene estos métodos.



| Método                                                  | Descripción                                                                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**ReadFromStream**](ijournalreader-readfromstream.md) | Toma una secuencia a un archivo de nota de diario y devuelve una secuencia XML que representa el contenido del documento.<br/> |



 

## <a name="remarks"></a>Comentarios

La **clase JournalReader** permite cargar una secuencia de documentos Journal y recibir una secuencia XML que representa el contenido. Puede reconstituir, mostrar y manipular la entrada de lápiz.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente de un controlador para el evento [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) de un botón se crea una instancia de la **clase JournalReader** y se usa para leer un archivo Journal existente.

> [!Note]  
> No se muestra el método **DisplayXml** al que se llama desde este ejemplo. La implementación específica de este método depende de las necesidades de la aplicación.

 


```C++
void CJntlReaderMFCDlg::OnBnClickedButton1()
{
  static TCHAR BASED_CODE szFilter[] = 
    _T("Journal files (*.jnt)|*.jnt|All files (*.*)|*.*");
  CFileDialog* fileDialog = new CFileDialog(TRUE, _T("*.jnt"), NULL, 
                                 OFN_FILEMUSTEXIST, szFilter, this);

  // Get the filename from the user via a File Open dialog
  if (fileDialog != NULL &&
      fileDialog->DoModal() == IDOK)
  {
    CString strFileName = fileDialog->GetPathName();

    // Read a JNT file into a memory buffer
    HANDLE hFile = CreateFile(strFileName,
                              GENERIC_READ,
                              FILE_SHARE_READ,
                              NULL,
                              OPEN_EXISTING,
                              FILE_ATTRIBUTE_NORMAL,
                              NULL);
    
    if (hFile != INVALID_HANDLE_VALUE)
    {
      // Allocate memory to hold the file contents
      DWORD dwFileSize = GetFileSize(hFile, NULL);
      HGLOBAL hGlobal = GlobalAlloc(GHND, dwFileSize);

      if (hGlobal != NULL)
      {
        LPBYTE pData = (LPBYTE)GlobalLock(hGlobal);

        if (pData != NULL)
        {
          DWORD dwRead;

          // Read the Journal file into the pData buffer
          if (ReadFile(hFile, pData, dwFileSize, &dwRead, NULL) &&
              (dwRead == dwFileSize))
          {
            HRESULT hr;
            IStream* pJntStream;

            // Create an IStream that points to the buffer
            hr = CreateStreamOnHGlobal(hGlobal, FALSE, &pJntStream);

            if (SUCCEEDED(hr))
            {
              IJournalReader* pJntReader;

              // Create a JournalReader object
              hr = CoCreateInstance(CLSID_JournalReader, NULL, CLSCTX_ALL, 
                          IID_IJournalReader, (void**)&pJntReader);

              if (SUCCEEDED(hr))
              {
                IStream* pXmlStream;

                // Read in the JNT file via the JournalReader
                hr = pJntReader->ReadFromStream(pJntStream, &pXmlStream);

                if (SUCCEEDED(hr))
                {
                  // Display results
                  DisplayXml(pXmlStream);

                  // Clean up
                  pXmlStream->Release();
                }
                pJntReader->Release();
              }
              pJntStream->Release();
            }
          }
          GlobalUnlock(hGlobal);
        }
        GlobalFree(hGlobal);
      }
      CloseHandle(hFile);
    }
    delete fileDialog;
  }
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                     |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                         |
| Header<br/>                   | <dl> <dt>Journal.h (también requiere journal \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Journal.dll</dt> </dl>                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[GUID de propiedad personalizada](custom-property-guids.md)
</dt> <dt>

[**ReadFromStream (método)**](ijournalreader-readfromstream.md)
</dt> </dl>

 

